<template>
  <div id="home">
    <radar-chart
      :options="chartOptions"
      :data="dataEnglishLevel"
    />
  </div>
</template>

<script>
  import RadarChart from './RadarChart.vue'

  export default {
    name: 'Home',
    components: {
      RadarChart
    },
    data() {
      return {
        chartOptions: {
          w: 290,				//Width of the circle
          h: 350,				//Height of the circle
          margin: { top: 50, right: 230, bottom: 50, left: 80 }, //The margins of the SVG
          levels: 5,				//How many levels or inner circles should there be drawn
          roundStrokes: false,  //If true the area and stroke will follow a round path (cardinal-closed)
          format: '.0f',        //labels format
          legend: { title: 'English Level of Front-End Department', translateX: 230, translateY: 40 },
          opacityArea: 0.35, 	//The opacity of the area of the blob
          dotRadius: 4, 			//The size of the colored circles of each blog
          opacityCircles: 0.1, 	//The opacity of the circles of each blob
          strokeWidth: 2, 		//The width of the stroke around each blob
        },
        colors: ["#2a2fd4", "#0099FF", "#33FFFF"],
        colors2: ["#AFC52F", "#ff6600", "#2a2fd4"],
        colors3: ["#26AF32", "#b90e0a", "#2a2fd4"],
        dataEnglishLevel: [
          {
            name: 'Alexandr',
            axes: [
              {
                axis: 'reading',
                value: 5,
              },
              {
                axis: 'grammar',
                value: 4,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 5,
              },
              {
                axis: 'writing',
                value: 4,
              },
              {
                axis: 'speaking',
                value: 4,
              }
            ]
          },
          {
            name: 'Dmitriy',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 5,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 5,
              },
              {
                axis: 'writing',
                value: 5,
              },
              {
                axis: 'speaking',
                value: 4,
              }
            ]
          },
          {
            name: 'Nikita',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 4,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 4,
              },
              {
                axis: 'writing',
                value: 4,
              },
              {
                axis: 'speaking',
                value: 4,
              }
            ]
          },
          {
            name: 'Olga',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 3,
              },
              {
                axis: 'vocabulary',
                value: 3,
              },
              {
                axis: 'listening',
                value: 5,
              },
              {
                axis: 'writing',
                value: 5,
              },
              {
                axis: 'speaking',
                value: 4,
              }
            ]
          },
          {
            name: 'Tatiana',
            axes: [
              {
                axis: 'reading',
                value: 5,
              },
              {
                axis: 'grammar',
                value: 4,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 5,
              },
              {
                axis: 'writing',
                value: 4,
              },
              {
                axis: 'speaking',
                value: 4,
              }
            ]
          },
          {
            name: 'Yevhenii',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 3,
              },
              {
                axis: 'vocabulary',
                value: 3,
              },
              {
                axis: 'listening',
                value: 4,
              },
              {
                axis: 'writing',
                value: 3,
              },
              {
                axis: 'speaking',
                value: 3,
              }
            ]
          },
          {
            name: 'Nikolay',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 4,
              },
              {
                axis: 'vocabulary',
                value: 3,
              },
              {
                axis: 'listening',
                value: 4,
              },
              {
                axis: 'writing',
                value: 3,
              },
              {
                axis: 'speaking',
                value: 3,
              }
            ]
          },
          {
            name: 'Vlada',
            axes: [
              {
                axis: 'reading',
                value: 5,
              },
              {
                axis: 'grammar',
                value: 4,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 5,
              },
              {
                axis: 'writing',
                value: 4,
              },
              {
                axis: 'speaking',
                value: 3,
              }
            ]
          },
          {
            name: 'Sergey',
            axes: [
              {
                axis: 'reading',
                value: 4,
              },
              {
                axis: 'grammar',
                value: 3,
              },
              {
                axis: 'vocabulary',
                value: 4,
              },
              {
                axis: 'listening',
                value: 4,
              },
              {
                axis: 'writing',
                value: 3,
              },
              {
                axis: 'speaking',
                value: 3,
              }
            ]
          },
        ],
        dataGoToTeam: [
          {
            name: 'Alexandr',
            axes: [
              {
                axis: 'English',
                value: 4,
              },
              {
                axis: 'Javascript',
                value: 4,
              },
              {
                axis: 'HTML',
                value: 5,
              },
              {
                axis: 'CSS',
                value: 5,
              },
              {
                axis: 'Vue',
                value: 4,
              },
              {
                axis: 'React',
                value: 2,
              },
            ]
          },
          {
            name: 'Dmitriy',
            axes: [
              {
                axis: 'English',
                value: 4,
              },
              {
                axis: 'Javascript',
                value: 5,
              },
              {
                axis: 'HTML',
                value: 5,
              },
              {
                axis: 'CSS',
                value: 5,
              },
              {
                axis: 'Vue',
                value: 5,
              },
              {
                axis: 'React',
                value: 3,
              },
            ]
          },
          {
            name: 'Yevhenii',
            axes: [
              {
                axis: 'English',
                value: 3,
              },
              {
                axis: 'Javascript',
                value: 3,
              },
              {
                axis: 'HTML',
                value: 4,
              },
              {
                axis: 'CSS',
                value: 5,
              },
              {
                axis: 'Vue',
                value: 2,
              },
              {
                axis: 'React',
                value: 1,
              },
            ]
          },
          {
            name: 'Nikita',
            axes: [
              {
                axis: 'English',
                value: 4,
              },
              {
                axis: 'Javascript',
                value: 4,
              },
              {
                axis: 'HTML',
                value: 5,
              },
              {
                axis: 'CSS',
                value: 4,
              },
              {
                axis: 'Vue',
                value: 1,
              },
              {
                axis: 'React',
                value: 4,
              },
            ]
          },
          {
            name: 'Olga',
            axes: [
              {
                axis: 'English',
                value: 4,
              },
              {
                axis: 'Javascript',
                value: 3,
              },
              {
                axis: 'HTML',
                value: 5,
              },
              {
                axis: 'CSS',
                value: 5,
              },
              {
                axis: 'Vue',
                value: 0,
              },
              {
                axis: 'React',
                value: 0,
              },
            ]
          },
          {
            name: 'Tatiana',
            axes: [
              {
                axis: 'English',
                value: 5,
              },
              {
                axis: 'Javascript',
                value: 3,
              },
              {
                axis: 'HTML',
                value: 4,
              },
              {
                axis: 'CSS',
                value: 4,
              },
              {
                axis: 'Vue',
                value: 2,
              },
              {
                axis: 'React',
                value: 0,
              },
            ]
          },
        ]
      }
    },
  }
</script>