---
UID: NF:wmp.IWMPControls.fastReverse
title: IWMPControls::fastReverse
author: windows-sdk-content
description: The fastReverse method starts fast play of the media item in the reverse direction.
old-location: wmp\iwmpcontrols_fastreverse.htm
tech.root: WMP
ms.assetid: 2adec4c7-7aca-4191-8c6f-61e137188ad9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls interface [Windows Media Player],fastReverse method, IWMPControls.fastReverse, IWMPControls::fastReverse, IWMPControlsfastReverse, fastReverse, fastReverse method [Windows Media Player], fastReverse method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_fastreverse, wmp/IWMPControls::fastReverse
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
 - IWMPControls.fastReverse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::fastReverse


## -description



The <b>fastReverse</b> method starts fast play of the media item in the reverse direction.




## -parameters






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



The <b>fastReverse</b> method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file. Calling <b>fastReverse</b> is equivalent to specifying -5.0 for the rate through the <b>IWMPSettings::put_rate</b> method. If the rate is subsequently changed, or if <b>IWMPControls::play</b> or <b>IWMPControls::stop</b> is called, Windows Media Player will cease fast reverse.

If the item is part of a playlist, <b>fastReverse</b> stops at the beginning of the current track. For instance, if track 3 is in <b>fastReverse</b>, when the beginning of track 3 is reached, Windows Media Player will not go to track 2. The play count is not incremented when calling <b>fastReverse</b>.

If you call <b>IWMPControls::fastForward</b> while <b>fastReverse</b> is running, <b>fastReverse</b> will be stopped and <b>IWMPControls::fastForward</b> will begin.

This method does not work for live broadcasts and certain digital media types. To determine whether you can use fast reverse in a clip, call the <b>IWMPControls::get_isAvailable</b> method and pass in the <b>BSTR</b> value "FastReverse".




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563179(v=VS.85).aspx">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563195(v=VS.85).aspx">IWMPControls::fastForward</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563201(v=VS.85).aspx">IWMPControls::get_isAvailable</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563205(v=VS.85).aspx">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563211(v=VS.85).aspx">IWMPControls::stop</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563680(v=VS.85).aspx">IWMPSettings::put_rate</a>
 

 

