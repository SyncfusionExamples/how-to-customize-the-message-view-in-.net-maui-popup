# how-to-customize-the-message-view-in-.net-maui-popup
The demo explains about how to customize the custom message view template in .NET MAUI Popup (SfPopup).

In .NET MAUI, the Popup control provides a flexible way to display transient content. It can be customized to include various elements such as buttons or even complex view. This article will guide you through the process of customizing the content of a .NET MAUI Popup using the ContentTemplate property.
For example you can display the Login page inside the .NET MAUI Popup refer the below.
XAML
    <StackLayout x:Name="mainLayout">
        <Button x:Name="clickToShowPopup"
                Text="ClickToShowPopup"
                VerticalOptions="Start"
                HorizontalOptions="FillAndExpand" />

        <sfPopup:SfPopup x:Name="popup"
                         AppearanceMode="TwoButton"
                         AcceptButtonText="Login"
                         DeclineButtonText="Cancel"
                         ShowHeader="False"
                         ShowFooter="True"
                         HeaderHeight="250">
            <sfPopup:SfPopup.ContentTemplate>
                <DataTemplate>
                    <StackLayout Padding="15">
                        <Entry Text="UserName"></Entry>
                        <Entry Text="Pasword"></Entry>
                    </StackLayout>
                </DataTemplate>
            </sfPopup:SfPopup.ContentTemplate>
        </sfPopup:SfPopup>
    </StackLayout>
