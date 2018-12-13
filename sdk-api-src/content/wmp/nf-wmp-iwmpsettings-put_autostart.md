---
UID: NF:wmp.IWMPSettings.put_autoStart
title: IWMPSettings::put_autoStart
author: windows-sdk-content
description: The put_autoStart method specifies a value indicating whether the current media item begins playing automatically.
old-location: wmp\iwmpsettings_put_autostart.htm
tech.root: WMP
ms.assetid: 34f80fa4-6e9c-4435-b360-55c2856f89fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_autoStart method, IWMPSettings.put_autoStart, IWMPSettings::put_autoStart, IWMPSettingsput_autoStart, put_autoStart, put_autoStart method [Windows Media Player], put_autoStart method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_autostart, wmp/IWMPSettings::put_autoStart
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.put_autoStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSettings::put_autoStart


## -description



The <b>put_autoStart</b> method specifies a value indicating whether the current media item begins playing automatically.




## -parameters




### -param fAutoStart [in]

<b>VARIANT_BOOL</b> indicating whether the current media item begins playing automatically. The default is <b>TRUE</b>.


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



The <b>put_autoStart</b> method for the full mode of Windows Media Player can be set globally by external events (such as loading a CD). Therefore, there is no reliable default value for skins and remoted Player controls. This is because the playback engine of the full mode Player is used in both cases.

You should set <b>put_autoStart</b> to <b>FALSE</b> immediately before you set <b>IWMPCore::put_URL</b>, <b>IWMPCore::put_currentPlaylist</b>, or <b>IWMPCore::put_currentMedia</b> in skins and remoted Player controls if you wish to ensure that the media item does not start playing immediately. Also, unless you set <b>put_autostart</b> to <b>TRUE</b> immediately before specifying a media item, you should not rely on this setting as a substitute for using the <b>IWMPControls::play</b> method.




## -see-also




<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">IWMPCore::put_currentMedia</a>



<a href="https://msdn.microsoft.com/943641ca-9733-4066-bc69-834e792d93dc">IWMPCore::put_currentPlaylist</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/37180d0a-8fc4-4fe6-b190-97258803b43b">IWMPSettings::get_autoStart</a>
 

 

