---
UID: NF:wmpplug.IWMPPluginUI.SetProperty
title: IWMPPluginUI::SetProperty
author: windows-sdk-content
description: The SetProperty method is called by Windows Media Player to set name/value property pairs for the plug-in.
old-location: wmp\iwmppluginui_setproperty.htm
tech.root: WMP
ms.assetid: 33b36239-3bda-44d3-8f85-7826bd8d3376
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPluginUI interface [Windows Media Player],SetProperty method, IWMPPluginUI.SetProperty, IWMPPluginUI::SetProperty, IWMPPluginUISetProperty, SetProperty, SetProperty method [Windows Media Player], SetProperty method [Windows Media Player],IWMPPluginUI interface, wmp.iwmppluginui_setproperty, wmpplug/IWMPPluginUI::SetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpplug.h
api_name:
 - IWMPPluginUI.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPluginUI::SetProperty


## -description



The <b>SetProperty</b> method is called by Windows Media Player to set name/value property pairs for the plug-in.




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
<td>The <i>pvarProperty</i> parameter contains a <b>Long</b> (<b>VT_I4</b>) value that specifies the index of the plug-in preset which is to be made current.</td>
</tr>
<tr>
<td>PLUGIN_ALL_MEDIASENDTO = L"MediaSendTo"</td>
<td>The <i>pvarProperty</i> parameter contains an array of <b>IUnknown</b> (<b>VT_ARRAY</b> | <b>VT_UNKNOWN</b>) pointers for <b>Media</b> objects that are sent to the plug-in from the Playlist control.</td>
</tr>
<tr>
<td>PLUGIN_ALL_PLAYLISTSENDTO = L"PlaylistSendTo"</td>
<td>The <i>pvarProperty</i> parameter contains an array of <b>IUnknown</b> (<b>VT_ARRAY</b> | <b>VT_UNKNOWN</b>) pointers for <b>Playlist</b> objects that are sent to the plug-in from the library.</td>
</tr>
</table>
 


### -param pvarProperty [in]

Pointer to a <b>VARIANT</b> containing the new value of the property.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player determines the type and capabilities of a plug-in by checking the Windows registry, and will specify only properties that the plug-in supports.

<b>Media</b> and <b>Playlist</b> objects are sent to the plug-in as arrays of <b>IUnknown</b> pointers. The plug-in can call <b>QueryInterface</b> on these pointers to retrieve <b>IWMPMedia</b> or <b>IWMPPlaylist</b> interfaces.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563591(v=VS.85).aspx">IWMPPluginUI Interface</a>



<a href="https://msdn.microsoft.com/45c1c760-808b-4d11-8e6b-057a2ca685d0">Media Object</a>
 

 

