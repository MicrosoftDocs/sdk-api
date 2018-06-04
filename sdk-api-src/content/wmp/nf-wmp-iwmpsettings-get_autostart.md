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

# IWMPSettings::get_autoStart


## -description



The <b>get_autoStart</b> method retrieves a value indicating whether the current media item begins playing automatically.




## -parameters




### -param pfAutoStart [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the current media item begins playing automatically. The default is <b>TRUE</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If <i>pfAutoStart</i> is <b>TRUE</b>, the media item will begin playing when <b>IWMPCore::put_URL</b>, <b>IWMPCore::put_currentPlaylist</b>, or <b>IWMPCore::put_currentMedia</b> is called. Otherwise, the media item will not start playing until the <b>IWMPControls::play</b> method is called.

<i>pfAutoStart</i> for the full mode of Windows Media Player can be set globally by external events (such as loading a CD). Skins and remoted Player controls cannot expect a default value because they both employ the full mode Windows Media Player playback engine.




## -see-also




<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">IWMPCore::put_currentMedia</a>



<a href="https://msdn.microsoft.com/943641ca-9733-4066-bc69-834e792d93dc">IWMPCore::put_currentPlaylist</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/34f80fa4-6e9c-4435-b360-55c2856f89fb">IWMPSettings::put_autoStart</a>
 

 

