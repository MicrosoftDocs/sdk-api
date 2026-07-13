---
UID: NF:wmpplug.IWMPPluginUI.GetProperty
title: IWMPPluginUI::GetProperty (wmpplug.h)
description: The GetProperty method is called by Windows Media Player to retrieve name/value property pairs from the plug-in.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Media Player]","GetProperty method [Windows Media Player]","IWMPPluginUI interface","IWMPPluginUI interface [Windows Media Player]","GetProperty method","IWMPPluginUI.GetProperty","IWMPPluginUI::GetProperty","IWMPPluginUIGetProperty","wmp.iwmppluginui_getproperty","wmpplug/IWMPPluginUI::GetProperty"]
old-location: wmp\iwmppluginui_getproperty.htm
tech.root: WMP
ms.assetid: f01d0700-2399-4e33-8a0c-59bb1f0f2495
ms.date: 4/26/2023
ms.keywords: GetProperty, GetProperty method [Windows Media Player], GetProperty method [Windows Media Player],IWMPPluginUI interface, IWMPPluginUI interface [Windows Media Player],GetProperty method, IWMPPluginUI.GetProperty, IWMPPluginUI::GetProperty, IWMPPluginUIGetProperty, wmp.iwmppluginui_getproperty, wmpplug/IWMPPluginUI::GetProperty
req.header: wmpplug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPPluginUI::GetProperty
 - wmpplug/IWMPPluginUI::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpplug.h
api_name:
 - IWMPPluginUI.GetProperty
---

# IWMPPluginUI::GetProperty


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProperty</b> method is called by Windows Media Player to retrieve name/value property pairs from the plug-in.

## -parameters

### -param pwszName [in]

Pointer to a <b>WCHAR</b><b>NULL</b>-terminated string constant containing the name of the property. Contains one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>PLUGIN_MISC_CURRENTPRESET = L"CurrentPreset"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value containing the index of the current preset. This property is requested only for plug-ins that have presets.</td>
</tr>
<tr>
<td>PLUGIN_MISC_PRESETCOUNT = L"PresetCount"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the number of presets available in the plug-in. This property is requested only for plug-ins that have presets.</td>
</tr>
<tr>
<td>PLUGIN_MISC_PRESETNAMES = L"PresetNames"</td>
<td>The out parameter is set to an array of <b>BSTR</b> (<b>VT_ARRAY</b> | <b>BSTR</b>) values containing the names of the presets. This property is requested only for plug-ins that have presets.</td>
</tr>
<tr>
<td>PLUGIN_MISC_QUERYDESTROY = L"QueryDestroy"</td>
<td>The out parameter is set to a <b>BSTR</b> (<b>VT_BSTR</b>) value that is displayed to the user when Windows Media Player attempts to close a separate window or background plug-in that is engaged in operations that cannot be interrupted.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_DEFAULTHEIGHT = L"DefaultHeight"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired default opening height of the plug-in window. This property is requested only for plug-ins in separate windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_DEFAULTWIDTH = L"DefaultWidth"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired default opening width of the plug-in window. This property is requested only for plug-ins in separate windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_MAXHEIGHT = L"MaxHeight"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired maximum height of the plug-in window. This property is requested only for plug-ins in separate, resizable windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_MAXWIDTH = L"MaxWidth"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired maximum width of the plug-in window. This property is requested only for plug-ins in separate, resizable windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_MINHEIGHT = L"MinHeight"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired minimum height of the plug-in window. This property is requested only for plug-ins in separate, resizable windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_MINWIDTH = L"MinWidth"</td>
<td>The out parameter is set to a <b>Long</b> (<b>VT_I4</b>) value indicating the desired minimum width of the plug-in window. This property is requested only for plug-ins in separate, resizable windows.</td>
</tr>
<tr>
<td>PLUGIN_SEPARATEWINDOW_RESIZABLE = L"Resizable"</td>
<td>The out parameter is set to a <b>Boolean</b> (<b>VT_BOOL</b>) value that indicates whether the plug-in window is resizable. This property is requested only for plug-ins in separate windows.</td>
</tr>
</table>

### -param pvarProperty [out]

Pointer to a <b>VARIANT</b> to contain the value of the property.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

Windows Media Player determines the type and capabilities of a plug-in by checking the Windows registry, and will retrieve only properties that the plug-in supports.

When a user attempts to close a separate window or background UI plug-in, or to close Windows Media Player when one of these plug-in types is active, this method is called with the <b>PLUGIN_MISC_QUERYDESTROY</b> property specified. If the plug-in is engaged in an operation that cannot be interrupted, such as reading or writing a file or waiting for user input in a modal dialog box, set the out parameter of this method to a non-empty value. This value is displayed to the user to indicate the problem. A user who is attempting to close Windows Media Player is then given the option of overriding the plug-in and closing the Player anyway.

When the plug-in is ready to close, set the out parameter to "" (empty string). When Windows Media Player calls this method and receives an empty value in the out parameter, it closes the plug-in without further delay.

This method is not called when a display area, settings area, or metadata area plug-in is closed. Because these plug-in types are displayed in the <b>Now Playing</b> pane, they must be ready to close at any time, such as when a user switches to another pane.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpplug/nn-wmpplug-iwmppluginui">IWMPPluginUI Interface</a>