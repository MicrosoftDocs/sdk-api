---
UID: NF:wmp.IWMPSettings.get_rate
title: IWMPSettings::get_rate
author: windows-sdk-content
description: The get_rate method retrieves the current playback rate for video.
old-location: wmp\iwmpsettings_get_rate.htm
old-project: WMP
ms.assetid: 1c3f2938-733f-42fc-ae07-66aad715958b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_rate method, IWMPSettings.get_rate, IWMPSettings::get_rate, IWMPSettingsget_rate, get_rate, get_rate method [Windows Media Player], get_rate method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_rate, wmp/IWMPSettings::get_rate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.get_rate
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::get_rate


## -description



The <b>get_rate</b> method retrieves the current playback rate for video.




## -parameters




### -param pdRate [out]

Pointer to a <b>double</b> containing the rate with a default value of 1.0.


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
<li><b>Windows Media Video (WMV) and ASF. </b>Optimal values for this property are from 1 to 10, or from –1 to –10 for reverse play. Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer. Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</li>
<li><b>Other video formats. </b>This property can range from 0 to 9. Negative values are not allowed. Values less than 1 represent slow motion. Values above 9 are allowed, but are not very meaningful.</li>
</ul>
The <b>IWMPControls::fastForward method</b> changes the value retrieved by <b>get_rate</b> to 5.0, while the <b>IWMPControls::fastReverse</b> method changes the value retrieved by <b>get_rate</b> to –5.0.

The playback rate of some digital media formats cannot be altered. Use the <b>IWMPSettings::get_isAvailable</b> method to determine whether this property can be specified for a particular media item.

<b>Windows Media Player 10 Mobile: </b>This method only retrieves a <b>long</b> set to -2.0, 1.0, or 2.0.




## -see-also




<a href="https://msdn.microsoft.com/a741da8d-f1a2-4a96-acb6-7c40077f6b5e">IWMPControls::fastForward</a>



<a href="https://msdn.microsoft.com/2adec4c7-7aca-4191-8c6f-61e137188ad9">IWMPControls::fastReverse</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/0773792f-4046-4d58-9673-cbfef0ec5bf5">IWMPSettings::get_isAvailable</a>



<a href="https://msdn.microsoft.com/b0bb1c84-d208-4d29-a797-bb18af039f03">IWMPSettings::get_mute</a>



<a href="https://msdn.microsoft.com/a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2">IWMPSettings::put_rate</a>
 

 

