<template>
  <Page class="container mx-auto bg-red-lighter">
    <ActionBar class="action-bar bg-blue-lighter" title="Lovely Seal Friends">
    </ActionBar>

   <ListView :items="seals">
        <v-template>
          <GridLayout class="py-4 px-4" columns="100, *" rows="20, 20, 20, *">
              <GridLayout col="0" row="0" rowSpan="4" rows="*">    
                <Image class="w-full rounded-full" :src="'~/images/'+item.img+'.jpg'" row="0"/>
              </GridLayout>
              <Label class="font-bold" :text="item.name" col="1" row="0 "/>
              <Label class="text-xs" :text="item.location" col="1" row="1"/>
              <Label class="text-xs text-right pr-4 text-grey-dark" text="1 day ago" col="1" row="1"/>        
              <Label textWrap="true" :text="item.description" col="1" row="3"/>
          </GridLayout>
        </v-template>
      </ListView>
  </Page>
</template>

<script>
export default {
	data() {
		return {
			seals: [
				{
					id: 1,
					img: 'leopard',
					name: 'Leopard Seal',
					location: 'Antarctica',
					description:
						'The leopard seal (Hydrurga leptonyx), also referred to as the sea leopard, is the second largest species of seal in the Antarctic',
				},
				{
					id: 2,
					img: 'harp',
					name: 'Harp Seal',
					location: 'Atlantic',
					description:
						'The harp seal or saddleback seal, Pagophilus groenlandicus is a species of earless seal, or true seal, native to the northernmost Atlantic Ocean and Arctic Ocean.',
				},
				{
					id: 3,
					img: 'harbor',
					name: 'Harbor Seal',
					location: 'Northern Hemisphere',
					description:
						'The harbor seal, also known as the common seal, is a true seal found along temperate and Arctic marine coastlines of the Northern Hemisphere.',
				},
				{
					id: 4,
					img: 'grey',
					name: 'Grey Seal',
					location: 'North Atlantic Ocean',
					description:
						'The grey seal is found on both shores of the North Atlantic Ocean. It is a large seal of the family Phocidae or "true seals". It is the only species classified in the genus Halichoerus.',
				},
				{
					id: 5,
					img: 'northern-elephant',
					name: 'Northern Elephant Seal',
					location: 'Northern Hemisphere',
					description:
						'The northern elephant seal is one of two species of elephant seal. It is a member of the family Phocidae.',
				},
				{
					id: 6,
					img: 'southern-elephant',
					name: 'Southern Elephant Seal',
					location: 'Southern Hemisphere',
					description:
						'The southern elephant seal is one of the two species of elephant seals. It is the largest member of the clade Pinnipedia and the order Carnivora, as well as the largest marine mammal that is not a cetacean.',
				},
				{
					id: 7,
					img: 'weddel',
					name: 'Weddel Seal',
					location: 'Antarctica',
					description:
						'The Weddell seal, Leptonychotes weddellii, is a relatively large and abundant true seal with a circumpolar distribution surrounding Antarctica.',
				},
				{
					id: 8,
					img: 'hawaiian-monk',
					name: 'Hawaiian Monk Seal',
					location: 'Hawaii',
					description:
						'The Hawaiian monk seal, Neomonachus schauinslandi, is an endangered species of earless seal in the family Phocidae that is endemic to the Hawaiian Islands.',
				},
				{
					id: 9,
					img: 'mediterranean-monk',
					name: 'Mediterranean Monk Seal',
					location: 'Mediterranean',
					description:
						'The Mediterranean monk seal is a monk seal belonging to the family Phocidae. As of 2015, it is estimated that fewer than 700 individuals survive in three or four isolated subpopulations in the Mediterranean.',
				},
			],
		};
	},
};
</script>

<style src="nativescript-tailwind/dist/tailwind.css"/>
