---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWMPPluginUI::SetProperty


## -description



The <b>SetProperty</b> method is called by Windows Media Player to set name/value property pairs for the plug-in.




## -parameters




### -param pwszName




### -param pvarProperty [in]

Pointer to a <b>VARIANT</b> containing the new value of the property.


#### - pswzName [in]

Pointer to a <b>WCHAR</b><b>NULL</b>-terminated string constant containing the name of the property. Contains one of the following values:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>
                  PLUGIN_MISC_CURRENTPRESET = L"CurrentPreset"</td>
<td>The <i>pvarProperty</i> parameter contains a <b>Long</b> (<b>VT_I4</b>) value that specifies the index of the plug-in preset which is to be made current.</td>
</tr>
<tr>
<td>
                  PLUGIN_ALL_MEDIASENDTO = L"MediaSendTo"</td>
<td>The <i>pvarProperty</i> parameter contains an array of <b>IUnknown</b> (<b>VT_ARRAY</b> | <b>VT_UNKNOWN</b>) pointers for <b>Media</b> objects that are sent to the plug-in from the Playlist control.</td>
</tr>
<tr>
<td>
                  PLUGIN_ALL_PLAYLISTSENDTO = L"PlaylistSendTo"</td>
<td>The <i>pvarProperty</i> parameter contains an array of <b>IUnknown</b> (<b>VT_ARRAY</b> | <b>VT_UNKNOWN</b>) pointers for <b>Playlist</b> objects that are sent to the plug-in from the library.</td>
</tr>
</table>
 


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player determines the type and capabilities of a plug-in by checking the Windows registry, and will specify only properties that the plug-in supports.

<b>Media</b> and <b>Playlist</b> objects are sent to the plug-in as arrays of <b>IUnknown</b> pointers. The plug-in can call <b>QueryInterface</b> on these pointers to retrieve <b>IWMPMedia</b> or <b>IWMPPlaylist</b> interfaces.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/f292a3e6-87bf-4e68-8737-f7d6351c4ff4">IWMPPluginUI Interface</a>



<a href="https://msdn.microsoft.com/45c1c760-808b-4d11-8e6b-057a2ca685d0">Media Object</a>
 

 

