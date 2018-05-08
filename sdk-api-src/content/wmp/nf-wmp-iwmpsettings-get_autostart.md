---
UID: NF:wmp.IWMPSettings.get_autoStart
title: IWMPSettings::get_autoStart
author: windows-driver-content
description: The get_autoStart method retrieves a value indicating whether the current media item begins playing automatically.
old-location: wmp\iwmpsettings_get_autostart.htm
old-project: WMP
ms.assetid: 37180d0a-8fc4-4fe6-b190-97258803b43b
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_autoStart method, IWMPSettings.get_autoStart, IWMPSettings::get_autoStart, IWMPSettingsget_autoStart, get_autoStart, get_autoStart method [Windows Media Player], get_autoStart method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_autostart, wmp/IWMPSettings::get_autoStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSettings.get_autoStart
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

