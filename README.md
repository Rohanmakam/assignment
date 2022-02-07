![WhatsApp Image 2022-02-07 at 5 27 37 PM](https://user-images.githubusercontent.com/98081951/152784498-da962577-0ec4-4d8a-93f5-e731a10fc2a7.jpeg)
![WhatsApp Image 2022-02-07 at 5 27 37 PM (2)](https://user-images.githubusercontent.com/98081951/152784507-674a2a67-7175-4ab9-aeda-25f019fc95b4.jpeg)

![WhatsApp Image 2022-02-07 at 5 27 37 PM (1)](https://user-images.githubusercontent.com/98081951/152784513-3e3c8ee9-1e09-4f7b-8cfc-dd0352baad75.jpeg)
import React from 'react';
import { useState } from 'react';
import { StyleSheet, Text, View,SafeAreaView ,ImageBackground,Image,TouchableOpacity,Button} from 'react-native';


import { ScrollView } from 'react-native';



const App = ()=> 
{
  const image= {uri:'src/images/back.png'}
    const[count,myCount]=useState(0);

 return (
     
      <View style={styles.container}>
        <ScrollView>
       
       <Text style={{textAlign:'center', marginTop:30,marginBottom:40,fontSize:20,padding:30,backgroundColor:'#ce9ffc'}}>COUNTER APPLICATION</Text>

       
       <TouchableOpacity
       style={styles.triangleShape}
       onPress={()=>{myCount(count+1)}}>
           <Text>press</Text>
     </TouchableOpacity>

     <Text style={{textAlign:'center', padding:30}}>{count}</Text>
   
     <TouchableOpacity
       style={styles.lowertriangle}
       onPress={()=>{myCount(count-1)}}>
           
     </TouchableOpacity>
     
     <TouchableOpacity title="reset" onPress={()=>{myCount(0)} 
      }  style={styles.reset}>
        
        
        <Text style={{fontSize:30}}>RESET</Text>
      </TouchableOpacity>

     
    </ScrollView>

    <Text style={styles.name}>Designed By ROHAN</Text>    
   </View>
      
  );
   
 }

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#feb672',
    //alignItems: 'center',
    //justifyContent: 'center',
  },
  triangleShape: {
    marginLeft:110,
  width: 0,
  height: 0,
  borderBottomWidth: 120,
  borderLeftWidth: 60,
  borderRightWidth: 60,
  backgroundColor: 'transparent',
  borderLeftColor: 'transparent',
  borderRightColor: 'transparent',
  borderBottomColor: '#f42e78'
},
lowertriangle: {
  marginLeft:110,
  width: 0,
  height: 0,
  borderTopWidth: 120,
  borderRightWidth: 60,
  borderLeftWidth: 60,
  borderRightColor: 'transparent',
  borderBottomColor: 'transparent',
  borderLeftColor: 'transparent',
  borderTopColor: "#f42e78",
},

reset:
{
  alignItems:'center',
  marginTop:50,
  marginRight:30,
 
},
icon:
{
  alignItems:'center',
  marginTop:-30,
  marginLeft:320,
  
},

name:
{
  textAlign:'center',
  
}



  
});

export default App;
