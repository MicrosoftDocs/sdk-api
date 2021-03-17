---
UID: NF:textstor.IAnchor.Shift
title: IAnchor::Shift (textstor.h)
description: The IAnchor::Shift method shifts the anchor forward or backward within a text stream.
helpviewer_keywords: ["IAnchor interface [Text Services Framework]","Shift method","IAnchor.Shift","IAnchor::Shift","Shift","Shift method [Text Services Framework]","Shift method [Text Services Framework]","IAnchor interface","TS_SHIFT_COUNT_ONLY","textstor/IAnchor::Shift","tsf.ianchor_shift"]
old-location: tsf\ianchor_shift.htm
tech.root: TSF
ms.assetid: e57a78e6-42e6-4a2b-b4e1-20bb64add872
ms.date: 12/05/2018
ms.keywords: IAnchor interface [Text Services Framework],Shift method, IAnchor.Shift, IAnchor::Shift, Shift, Shift method [Text Services Framework], Shift method [Text Services Framework],IAnchor interface, TS_SHIFT_COUNT_ONLY, textstor/IAnchor::Shift, tsf.ianchor_shift
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IAnchor::Shift
 - textstor/IAnchor::Shift
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.Shift
---

# IAnchor::Shift


## -description

The <b>IAnchor::Shift</b> method shifts the anchor forward or backward within a text stream.

## -parameters

### -param dwFlags [in]

Bit fields that are used to avoid anchor positioning.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_SHIFT_COUNT_ONLY"></a><a id="ts_shift_count_only"></a><dl>
<dt><b>TS_SHIFT_COUNT_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The anchor is not shifted. If the flag is not set (<i>dwFlags</i> = 0), the anchor will be shifted as specified by the other parameter settings.

</td>
</tr>
</table>

### -param cchReq [in]

The number of characters to move the anchor within the text stream.

### -param pcch [out]

The actual number of characters moved within the text stream. The method will set <i>pcch</i> to zero if it fails.

### -param paHaltAnchor [in]

Reference to an anchor that blocks the shift. Set to <b>NULL</b> to avoid blocking the shift.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The shift failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An input parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter value is not implemented in this method.

</td>
</tr>
</table>

## -remarks

<i>cchReq</i> and <i>pcch</i> parameters can be negative, meaning a shift backward in the text stream, or positive, meaning a shift forward. The actual number of characters shifted can be less than <i>cchReq</i> if the beginning or end of the document is encountered, a region boundary is encountered, or if <i>paHaltAnchor</i> receives an anchor that blocks the shift.

If <i>paHaltAnchor</i> receives an anchor that blocks the shift, the application will truncate the shift at the position occupied by <i>paHaltAnchor.</i> If <i>paHaltAnchor</i> is not within the span of text covered by the shift, it has no relevance to the shift and is ignored.

For example, if the anchor referenced by <i>paHaltAnchor</i> lies 8 characters ahead of the anchor in the stream, and a client calls <b>Shift</b> (0, 10, pcch, paHaltAnchor), then on exit the anchor will have moved only 8 characters. If the anchor referenced by <i>paHaltAnchor</i> is equal to the current anchor to be moved, then <b>Shift</b> will return successfully without moving the anchor at all. In this case <i>pcch</i> will be 0.

The anchor shift is always blocked by region boundaries, as if the beginning or end of the document were encountered. This will be indicated on exit by the actual shift <i>pcch</i> being smaller in absolute value than the requested shift <i>cchReq</i>. In this case, clients can use <a href="/windows/desktop/api/textstor/nf-textstor-ianchor-shiftregion">IAnchor::ShiftRegion</a> to shift the anchor into an adjacent region.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-shiftregion">IAnchor::ShiftRegion
      </a>