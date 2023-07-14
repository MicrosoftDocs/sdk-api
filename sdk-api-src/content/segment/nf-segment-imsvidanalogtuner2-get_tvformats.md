---
UID: NF:segment.IMSVidAnalogTuner2.get_TVFormats
title: IMSVidAnalogTuner2::get_TVFormats (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IMSVidAnalogTuner2 interface [Microsoft TV Technologies]","get_TVFormats method","IMSVidAnalogTuner2.get_TVFormats","IMSVidAnalogTuner2::get_TVFormats","IMSVidAnalogTuner2getTVFormats","get_TVFormats","get_TVFormats method [Microsoft TV Technologies]","get_TVFormats method [Microsoft TV Technologies]","IMSVidAnalogTuner2 interface","mstv.imsvidanalogtuner2_get_tvformats","segment/IMSVidAnalogTuner2::get_TVFormats"]
old-location: mstv\imsvidanalogtuner2_get_tvformats.htm
tech.root: mstv
ms.assetid: 82816d89-0a15-4868-8e86-12b683de03b1
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner2 interface [Microsoft TV Technologies],get_TVFormats method, IMSVidAnalogTuner2.get_TVFormats, IMSVidAnalogTuner2::get_TVFormats, IMSVidAnalogTuner2getTVFormats, get_TVFormats, get_TVFormats method [Microsoft TV Technologies], get_TVFormats method [Microsoft TV Technologies],IMSVidAnalogTuner2 interface, mstv.imsvidanalogtuner2_get_tvformats, segment/IMSVidAnalogTuner2::get_TVFormats
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
 - IMSVidAnalogTuner2::get_TVFormats
 - segment/IMSVidAnalogTuner2::get_TVFormats
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
 - IMSVidAnalogTuner2.get_TVFormats
---

# IMSVidAnalogTuner2::get_TVFormats


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_TVFormats</b> method retrieves a flag value that indicates which TV formats the tuner supports, such as NTSC, PAL, or SECAM.

## -parameters

### -param Formats [out]

Pointer to a variable that receives the formats flag. Possible values are the sum of one or more of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0x00000000</td>
<td>Digital sensor</td>
</tr>
<tr>
<td>0x00000001</td>
<td>NTSC (M) standard, 7.5 IRE black</td>
</tr>
<tr>
<td>0x00000002</td>
<td>NTSC (M) standard, 0 IRE black (Japan)</td>
</tr>
<tr>
<td>0x00000004</td>
<td>NTSC-433</td>
</tr>
<tr>
<td>0x00000010</td>
<td>PAL-B standard</td>
</tr>
<tr>
<td>0x00000020</td>
<td>PAL (D) standard</td>
</tr>
<tr>
<td>0x00000080</td>
<td>PAL (H) standard</td>
</tr>
<tr>
<td>0x00000100</td>
<td>PAL (I) standard</td>
</tr>
<tr>
<td>0x00000200</td>
<td>PAL (M) standard</td>
</tr>
<tr>
<td>0x00000400</td>
<td>PAL (N) standard</td>
</tr>
<tr>
<td>0x00000800</td>
<td>PAL-60 standard</td>
</tr>
<tr>
<td>0x00001000</td>
<td>SECAM (B) standard</td>
</tr>
<tr>
<td>0x00002000</td>
<td>SECAM (D) standard</td>
</tr>
<tr>
<td>0x00004000</td>
<td>SECAM (G) standard</td>
</tr>
<tr>
<td>0x00008000</td>
<td>SECAM (H) standard</td>
</tr>
<tr>
<td>0x00010000</td>
<td>SECAM (K) standard</td>
</tr>
<tr>
<td>0x00020000</td>
<td>SECAM (K1) standard</td>
</tr>
<tr>
<td>0x00040000</td>
<td>SECAM (L) standard</td>
</tr>
<tr>
<td>0x00080000</td>
<td>SECAM (L1) standard</td>
</tr>
<tr>
<td>0x00100000</td>
<td>Combination (N) PAL standard (Argentina)</td>
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