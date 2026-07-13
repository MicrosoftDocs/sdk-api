---
UID: NF:segment.IMSVidAnalogTuner2.get_TunerModes
title: IMSVidAnalogTuner2::get_TunerModes (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IMSVidAnalogTuner2 interface [Microsoft TV Technologies]","get_TunerModes method","IMSVidAnalogTuner2.get_TunerModes","IMSVidAnalogTuner2::get_TunerModes","IMSVidAnalogTuner2getTunerModes","get_TunerModes","get_TunerModes method [Microsoft TV Technologies]","get_TunerModes method [Microsoft TV Technologies]","IMSVidAnalogTuner2 interface","mstv.imsvidanalogtuner2_get_tunermodes","segment/IMSVidAnalogTuner2::get_TunerModes"]
old-location: mstv\imsvidanalogtuner2_get_tunermodes.htm
tech.root: mstv
ms.assetid: dc5652d4-aa1d-480e-a5f4-05ed9d9b1887
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner2 interface [Microsoft TV Technologies],get_TunerModes method, IMSVidAnalogTuner2.get_TunerModes, IMSVidAnalogTuner2::get_TunerModes, IMSVidAnalogTuner2getTunerModes, get_TunerModes, get_TunerModes method [Microsoft TV Technologies], get_TunerModes method [Microsoft TV Technologies],IMSVidAnalogTuner2 interface, mstv.imsvidanalogtuner2_get_tunermodes, segment/IMSVidAnalogTuner2::get_TunerModes
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
 - IMSVidAnalogTuner2::get_TunerModes
 - segment/IMSVidAnalogTuner2::get_TunerModes
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
 - IMSVidAnalogTuner2.get_TunerModes
---

# IMSVidAnalogTuner2::get_TunerModes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_TunerModes</b> method retrieves a flag value that indicates which modes the tuner supports, such as TV or FM.

## -parameters

### -param Modes [out]

Pointer to a variable that receives the modes flag. Possible values are the sum of one or more of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0x0000</td>
<td>Default tuner mode.</td>
</tr>
<tr>
<td>0x0001</td>
<td>TV tuner mode.</td>
</tr>
<tr>
<td>0x0002</td>
<td>FM radio tuner mode.</td>
</tr>
<tr>
<td>0x0004</td>
<td>AM radio tuner mode.</td>
</tr>
</table>

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner2">IMSVidAnalogTuner2 Interface</a>