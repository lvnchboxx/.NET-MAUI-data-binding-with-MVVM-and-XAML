# UI
![image](https://user-images.githubusercontent.com/81525850/225427560-0dcdb493-350a-4704-8348-476a02c43c61.png)

<details><summary>Code</summary>
<p>

```Grid RowDefinitions="100, Auto, *"
          ColumnDefinitions=".75*, .25*"
          Padding="10"
          RowSpacing="10"
          ColumnSpacing="10">

        <Image Grid.ColumnSpan="2"
               Source="takasi.png"
               BackgroundColor="#24701D"/>

        <Entry Placeholder="Enter task"
               Text="{Binding Text}"
               Grid.Row="1"/>

        <Button Text="Add"
                Command="{Binding AddCommand}"
                Grid.Row="1"
                Grid.Column="1"
                BackgroundColor="DarkSeaGreen"/>
```

</p>
</details>

# Addidng items
![image](https://user-images.githubusercontent.com/81525850/225427887-960fb883-3f11-4a2a-a1f3-b33bf9d24ea9.png)
as you can see i add my Name and Student ID as an item



# ViewDetails
![image](https://user-images.githubusercontent.com/81525850/225428041-4257ddcf-7902-4fbc-b7e2-3b7694ae393b.png)
You can click this and see a viewdetails page

<details><summary>Code</summary>
<p>



```<TapGestureRecognizer 
                                           Command="{Binding Source={RelativeSource AncestorType={x:Type viewmodel:MainViewModel}}, Path=TapCommand}"
                                           CommandParameter="{Binding .}"/>
```

</p>
</details>

# Connectivity

![image](https://user-images.githubusercontent.com/81525850/225428251-fce867d5-8fcc-4a06-bcc8-1c66b86f904d.png)
When the Connectivity is terminated a pop up will show up

<details><summary>Code</summary>
<p>



```if(connectivity.NetworkAccess != NetworkAccess.Internet)
        {
            await Shell.Current.DisplayAlert("woops!", "I Guess u r disconnected", "OK");
            return;
        }
```

</p>
</details>
