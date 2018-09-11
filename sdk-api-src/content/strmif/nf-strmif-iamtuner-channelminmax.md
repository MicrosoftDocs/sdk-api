---
UID: NF:strmif.IAMTuner.ChannelMinMax
title: IAMTuner::ChannelMinMax
author: windows-sdk-content
description: The ChannelMinMax method retrieves the highest and lowest channels available.
old-location: dshow\iamtuner_channelminmax.htm
tech.root: DirectShow
ms.assetid: f46bf0ff-cdb3-41b1-829e-4e1b348bd808
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ChannelMinMax, ChannelMinMax method [DirectShow], ChannelMinMax method [DirectShow],IAMTuner interface, IAMTuner interface [DirectShow],ChannelMinMax method, IAMTuner.ChannelMinMax, IAMTuner::ChannelMinMax, IAMTunerChannelMinMax, dshow.iamtuner_channelminmax, strmif/IAMTuner::ChannelMinMax
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.ChannelMinMax
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner::ChannelMinMax


## -description



The <code>ChannelMinMax</code> method retrieves the highest and lowest channels available.




## -parameters




### -param lChannelMin [out]

Pointer to a variable that receives the lowest channel.


### -param lChannelMax [out]

Pointer to a variable that receives the highest channel.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>



<a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>
 

 

