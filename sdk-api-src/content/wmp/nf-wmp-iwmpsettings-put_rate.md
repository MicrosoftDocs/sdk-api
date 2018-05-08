---
UID: NF:wmp.IWMPSettings.put_rate
title: IWMPSettings::put_rate
author: windows-driver-content
description: The put_rate method specifies the current playback rate for video.
old-location: wmp\iwmpsettings_put_rate.htm
old-project: WMP
ms.assetid: a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_rate method, IWMPSettings.put_rate, IWMPSettings::put_rate, IWMPSettingsput_rate, put_rate, put_rate method [Windows Media Player], put_rate method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_rate, wmp/IWMPSettings::put_rate
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
-	IWMPSettings.put_rate
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_rate


## -description



The <b>put_rate</b> method specifies the current playback rate for video.




## -parameters




### -param dRate [in]

<b>double</b> containing the rate with a default value of 1.0.


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



The value retrieved by this method acts as a multiplier value that enables you to play a media item at a faster or slower rate. The default value of 1.0 indicates the authored speed.

Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5. A playback rate of 2 equates to twice the normal playback speed.

Windows Media Player will attempt to use the most effective of the following four different playback modes

<ul>
<li>Smooth video playback with audio pitch maintained</li>
<li>Smooth video playback with audio pitch not maintained</li>
<li>Smooth video playback with no audio</li>
<li>Keyframe video playback with no audio</li>
</ul>
The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.

Other considerations apply as well, depending on the digital media format used to create the content:

<ul>
<li>Windows Media Video (WMV) and ASF. Optimal values for this property are from 1 to 10, or from –1 to –10 for reverse play. Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer. Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</li>
<li><b>Other video formats. </b>This property can range from 0 to 9. Negative values are not allowed. Values less than 1 represent slow motion. Values above 9 are allowed, but are not very meaningful.</li>
</ul>
The <b>IWMPControls::fastForward</b> method changes the value retrieved by <b>get_rate</b> to 5.0, while the <b>IWMPControls::fastReverse</b> method changes the value retrieved by <b>get_rate</b> to –5.0.

The playback rate of some digital media formats cannot be altered. Use the <b>IWMPSettings::get_isAvailable</b> method to determine whether this property can be specified for a particular media item.

<b>Windows Media Player 10 Mobile: </b>This method only accepts a <b>long</b> set to -5.0, 1.0, or 5.0. Otherwise, E_INVALIDARG is returned.




## -see-also




<a href="https://msdn.microsoft.com/a741da8d-f1a2-4a96-acb6-7c40077f6b5e">IWMPControls::fastForward</a>



<a href="https://msdn.microsoft.com/2adec4c7-7aca-4191-8c6f-61e137188ad9">IWMPControls::fastReverse</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/0773792f-4046-4d58-9673-cbfef0ec5bf5">IWMPSettings::get_isAvailable</a>



<a href="https://msdn.microsoft.com/1c3f2938-733f-42fc-ae07-66aad715958b">IWMPSettings::get_rate</a>



<a href="https://msdn.microsoft.com/644f9a4d-54e4-4e8a-8c02-29feb57c9256">IWMPSettings::put_mute</a>
 

 

