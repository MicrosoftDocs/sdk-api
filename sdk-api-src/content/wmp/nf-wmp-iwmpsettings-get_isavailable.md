---
UID: NF:wmp.IWMPSettings.get_isAvailable
title: IWMPSettings::get_isAvailable
author: windows-sdk-content
description: The get_isAvailable method indicates whether a specified action can be performed.
old-location: wmp\iwmpsettings_get_isavailable.htm
tech.root: WMP
ms.assetid: 0773792f-4046-4d58-9673-cbfef0ec5bf5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_isAvailable method, IWMPSettings.get_isAvailable, IWMPSettings::get_isAvailable, IWMPSettingsget_isAvailable, get_isAvailable, get_isAvailable method [Windows Media Player], get_isAvailable method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_isavailable, wmp/IWMPSettings::get_isAvailable
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
 - IWMPSettings.get_isAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSettings::get_isAvailable


## -description



The <b>get_isAvailable</b> method indicates whether a specified action can be performed.




## -parameters




### -param bstrItem [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AutoStart</td>
<td>Determines whether the <b>put_autoStart</b> method can be used to specify that Windows Media Player starts playback automatically.</td>
</tr>
<tr>
<td>Balance</td>
<td>Determines whether the <b>put_balance</b> method can be used to set the stereo balance.</td>
</tr>
<tr>
<td>BaseURL</td>
<td>Determines whether the <b>put_baseURL</b> method can be used to specify a base URL.</td>
</tr>
<tr>
<td>DefaultFrame</td>
<td>Determines whether the <b>put_defaultFrame</b> method can be used to specify the default frame.</td>
</tr>
<tr>
<td>EnableErrorDialogs</td>
<td>Determines whether the <b>put_enableErrorDialogs</b> method can be used to enable or disable displaying error dialog boxes.</td>
</tr>
<tr>
<td>GetMode</td>
<td>Determines whether the <b>getMode</b> method can be used to retrieve the current loop or shuffle mode.</td>
</tr>
<tr>
<td>InvokeURLs</td>
<td>Determines whether the <b>put_invokeURLs</b> method can be used to specify whether URL events should launch a Web browser.</td>
</tr>
<tr>
<td>Mute</td>
<td>Determines whether the <b>put_mute</b> method can be used to specify whether the audio output is on or off.</td>
</tr>
<tr>
<td>PlayCount</td>
<td>Determines whether the <b>put_playCount</b> method can be used to specify the number times a media item will play.</td>
</tr>
<tr>
<td>Rate</td>
<td>Determines whether the <b>put_rate</b> method can be used to set the playback rate.</td>
</tr>
<tr>
<td>SetMode</td>
<td>Determines whether the <b>setMode</b> method can be used to specify the current loop or shuffle mode.</td>
</tr>
<tr>
<td>Volume</td>
<td>Determines whether the <b>put_volume</b> method can be used to specify the audio volume.</td>
</tr>
</table>
 


### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the specified action can be performed.


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
 




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/5275cb99-8007-4af2-9137-694de18c5434">IWMPSettings::getMode</a>



<a href="https://msdn.microsoft.com/34f80fa4-6e9c-4435-b360-55c2856f89fb">IWMPSettings::put_autoStart</a>



<a href="https://msdn.microsoft.com/bb198bc0-a0cf-4f6b-9a1e-f9a552db7092">IWMPSettings::put_balance</a>



<a href="https://msdn.microsoft.com/ae070004-e90e-4f1e-b8b8-15deccdc48ad">IWMPSettings::put_baseURL</a>



<a href="https://msdn.microsoft.com/9b035e4e-84c5-46ea-aa8a-2e66810284b2">IWMPSettings::put_defaultFrame</a>



<a href="https://msdn.microsoft.com/c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393">IWMPSettings::put_enableErrorDialogs</a>



<a href="https://msdn.microsoft.com/4c62ba8e-8fca-4cfe-9a52-6b6ac2c7c0de">IWMPSettings::put_invokeURLs</a>



<a href="https://msdn.microsoft.com/644f9a4d-54e4-4e8a-8c02-29feb57c9256">IWMPSettings::put_mute</a>



<a href="https://msdn.microsoft.com/b9fdd596-8ca3-497e-8d40-6dd5ddbf0a1e">IWMPSettings::put_playCount</a>



<a href="https://msdn.microsoft.com/a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2">IWMPSettings::put_rate</a>



<a href="https://msdn.microsoft.com/435dac36-1ccf-41fd-94c2-1242c6af1bbd">IWMPSettings::put_volume</a>



<a href="https://msdn.microsoft.com/28a404a7-5bb0-41bb-a5b2-cc6138b8176e">IWMPSettings::setMode</a>
 

 

