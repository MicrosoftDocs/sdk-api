---
UID: NF:segment.IMSVidAnalogTuner2.get_NumAuxInputs
title: IMSVidAnalogTuner2::get_NumAuxInputs (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IMSVidAnalogTuner2 interface [Microsoft TV Technologies]","get_NumAuxInputs method","IMSVidAnalogTuner2.get_NumAuxInputs","IMSVidAnalogTuner2::get_NumAuxInputs","IMSVidAnalogTuner2getNumAuxInputs","get_NumAuxInputs","get_NumAuxInputs method [Microsoft TV Technologies]","get_NumAuxInputs method [Microsoft TV Technologies]","IMSVidAnalogTuner2 interface","mstv.imsvidanalogtuner2_get_numauxinputs","segment/IMSVidAnalogTuner2::get_NumAuxInputs"]
old-location: mstv\imsvidanalogtuner2_get_numauxinputs.htm
tech.root: mstv
ms.assetid: 72e3c0eb-4c65-4782-b799-80bf968e736a
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner2 interface [Microsoft TV Technologies],get_NumAuxInputs method, IMSVidAnalogTuner2.get_NumAuxInputs, IMSVidAnalogTuner2::get_NumAuxInputs, IMSVidAnalogTuner2getNumAuxInputs, get_NumAuxInputs, get_NumAuxInputs method [Microsoft TV Technologies], get_NumAuxInputs method [Microsoft TV Technologies],IMSVidAnalogTuner2 interface, mstv.imsvidanalogtuner2_get_numauxinputs, segment/IMSVidAnalogTuner2::get_NumAuxInputs
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAnalogTuner2::get_NumAuxInputs
 - segment/IMSVidAnalogTuner2::get_NumAuxInputs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner2.get_NumAuxInputs
---

# IMSVidAnalogTuner2::get_NumAuxInputs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner2">IMSVidAnalogTuner2 Interface</a>