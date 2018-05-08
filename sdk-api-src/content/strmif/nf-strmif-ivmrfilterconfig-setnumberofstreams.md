---
UID: NF:strmif.IVMRFilterConfig.SetNumberOfStreams
title: IVMRFilterConfig::SetNumberOfStreams
author: windows-driver-content
description: The SetNumberOfStreams method sets the number of streams to be mixed and instructs the VMR to go into mixer mode.
old-location: dshow\ivmrfilterconfig_setnumberofstreams.htm
old-project: DirectShow
ms.assetid: cd200b33-bb74-474a-9047-d81cb470af23
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetNumberOfStreams method, IVMRFilterConfig.SetNumberOfStreams, IVMRFilterConfig::SetNumberOfStreams, IVMRFilterConfigSetNumberOfStreams, SetNumberOfStreams, SetNumberOfStreams method [DirectShow], SetNumberOfStreams method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setnumberofstreams, strmif/IVMRFilterConfig::SetNumberOfStreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRFilterConfig.SetNumberOfStreams
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRFilterConfig::SetNumberOfStreams


## -description



The <code>SetNumberOfStreams</code> method sets the number of streams to be mixed and instructs the VMR to go into mixer mode.




## -parameters




### -param dwMaxStreams [in]

Double word containing the maximum number of input streams that the VMR will be required to mix. Must not be greater than MAX_MIXER_STREAMS (16).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The mixer is already configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to configure the mixer for more than 16 input streams.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory to manage the streams could not be allocated.

</td>
</tr>
</table>
 




## -remarks



<i>dwMaxStreams</i> should be equal to the number of input pins required. Pins cannot be added or removed after the VMR has been connected. If you do not know in advance how many input streams will be required, set <i>dxMaxStreams</i> to the maximum number that might be required. A value of 1 is valid for dwMaxStreams. This value does not cause any extra pins to be created, but it does force the VMR to go into "mixer mode." Therefore, once this method has been called, you cannot call <a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">SetRenderingMode</a> to set the mode to <b>VMRMode_Renderless</b>

The VMR creates as many input pins as are specified without attempting to determine whether there is enough video memory to support them all. This is because it has no way of knowing the media type or rectangle dimensions at this time. Later, when an upstream filter attempts to connect to a pin, at that point the media type is known and the VMR will examine the video memory and fail the connection if there is not enough to process the stream.

<div class="alert"><b>Note</b>  Although the VMR supports multiple streams, they all share a single clock, and therefore you cannot seek one stream independently of the others. If you need to seek the input streams independently, you must use a different technique. See the VMRMulti sample for more information.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/e031c427-23bb-4243-bb38-0837a6db8c2c">IVMRFilterConfig::GetNumberOfStreams</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

