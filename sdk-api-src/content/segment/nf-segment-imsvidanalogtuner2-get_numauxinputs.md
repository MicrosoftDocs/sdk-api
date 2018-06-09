---
UID: NF:segment.IMSVidAnalogTuner2.get_NumAuxInputs
title: IMSVidAnalogTuner2::get_NumAuxInputs
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\imsvidanalogtuner2_get_numauxinputs.htm
old-project: mstv
ms.assetid: 72e3c0eb-4c65-4782-b799-80bf968e736a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidAnalogTuner2 interface [Microsoft TV Technologies],get_NumAuxInputs method, IMSVidAnalogTuner2.get_NumAuxInputs, IMSVidAnalogTuner2::get_NumAuxInputs, IMSVidAnalogTuner2getNumAuxInputs, get_NumAuxInputs, get_NumAuxInputs method [Microsoft TV Technologies], get_NumAuxInputs method [Microsoft TV Technologies],IMSVidAnalogTuner2 interface, mstv.imsvidanalogtuner2_get_numauxinputs, segment/IMSVidAnalogTuner2::get_NumAuxInputs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner2.get_NumAuxInputs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidAnalogTuner2::get_NumAuxInputs


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_NumAuxInputs</b> method retrieves the number of auxiliary inputs that are available. Auxiliary inputs include S-video and composite inputs.


## -parameters




### -param Inputs [out]

Pointer to a variable that receives the number of auxiliary inputs.


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
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



A crossbar filter exposes two auxiliary inputs for each audio input that it supports. That is, each audio input pin has two corresponding auxiliary input pins: S-video and composite video.

The number of auxiliary inputs returned by this method includes all auxiliary inputs, even if the physical input jacks are combined in some manner (for example, with some sort of proprietary or overloaded jack).

The first S-video input is channel 0 and the first composite input is channel 1. Additional S-video inputs are on even-numbered channels and additional composite inputs are on odd-numbered channels.




## -see-also




<a href="https://msdn.microsoft.com/50d30a45-8cea-454c-b5d2-ff809b8a8206">IMSVidAnalogTuner2 Interface</a>
 

 

