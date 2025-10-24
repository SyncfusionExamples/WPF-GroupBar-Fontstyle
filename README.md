# WPF GroupBar – Customize Header Font Style
## Overview
The GroupBar control is a navigation component that organizes content into expandable groups, commonly used in applications for structured navigation. This repository demonstrates how to customize the font style of GroupBarItem headers in the Syncfusion WPF GroupBar using the HeaderTemplate property. By default, the header text uses the system font style, but you can override this to match your application’s theme or branding.

## Why customize the font style?
- Maintain visual consistency with your app’s theme
- Emphasize important navigation sections
- Improve accessibility with larger fonts and better contrast

## Prerequisites
- WPF application (.NET Framework or .NET Desktop)
- Syncfusion WPF controls installed
    - NuGet: Syncfusion.Shared.WPF and related packages for GroupBar
- XAML namespace
    - xmlns:syncfusion="http://schemas.syncfusion.com/wpf"

## Key implementation steps
- Use GroupBarItem.HeaderTemplate to override the default header look
- Define a DataTemplate with a TextBlock (or any custom element)
- Set font properties such as FontFamily, FontSize, FontWeight, FontStyle, and Foreground
- Bind the header text:
    - If Header is a string: Text="{Binding}"
    - If Header is an object: Text="{Binding YourProperty}"

### Example XAML:
```xml
<syncfusion:GroupBar>
    <syncfusion:GroupBarItem Header="Documents">
        <syncfusion:GroupBarItem.HeaderTemplate>
            <DataTemplate>
                <TextBlock Text="{Binding}" FontFamily="Segoe UI" FontSize="16" FontWeight="Bold" Foreground="DarkBlue"/>
            </DataTemplate>
        </syncfusion:GroupBarItem.HeaderTemplate>
    </syncfusion:GroupBarItem>
</syncfusion:GroupBar>
```
This approach gives you full control over the header’s appearance, allowing you to create a polished and professional UI. For detailed instructions and additional examples, refer to the official KB article - [WPF-GroupBar-Fontstyle](https://www.syncfusion.com/kb/11716/how-to-override-groupbaritemheader-font-in-wpf-groupbar)
