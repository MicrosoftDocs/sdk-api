---
UID: NF:sbe.IEnumStreamBufferRecordingAttrib.Next
title: IEnumStreamBufferRecordingAttrib::Next (sbe.h)
description: The Next method returns a specified number of attributes in the enumeration sequence.
helpviewer_keywords: ["IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies]","Next method","IEnumStreamBufferRecordingAttrib.Next","IEnumStreamBufferRecordingAttrib::Next","IEnumStreamBufferRecordingAttribNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumStreamBufferRecordingAttrib interface","mstv.ienumstreambufferrecordingattrib_next","sbe/IEnumStreamBufferRecordingAttrib::Next"]
old-location: mstv\ienumstreambufferrecordingattrib_next.htm
tech.root: mstv
ms.assetid: 760b2e2c-799d-45e5-9dbd-2407e7431918
ms.date: 12/05/2018
ms.keywords: IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],Next method, IEnumStreamBufferRecordingAttrib.Next, IEnumStreamBufferRecordingAttrib::Next, IEnumStreamBufferRecordingAttribNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumStreamBufferRecordingAttrib interface, mstv.ienumstreambufferrecordingattrib_next, sbe/IEnumStreamBufferRecordingAttrib::Next
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumStreamBufferRecordingAttrib::Next
 - sbe/IEnumStreamBufferRecordingAttrib::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IEnumStreamBufferRecordingAttrib.Next
---

# IEnumStreamBufferRecordingAttrib::Next


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Next</b> method returns a specified number of attributes in the enumeration sequence.

## -parameters

### -param cRequest [in]

The number of attributes to retrieve.

### -param pStreamBufferAttribute [in, out]

Pointer to an array of size <i>cRequest</i>. The array is filled with <a href="/previous-versions/windows/desktop/api/sbe/ns-sbe-streambuffer_attribute">STREAMBUFFER_ATTRIBUTE</a> structures.

### -param pcReceived [out]

Pointer to a variable that receives the number of attributes that are returned in the <i>pStreamBufferAttribute</i> array. This parameter can be <b>NULL</b> if <i>cRequest</i> is 1.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Did not retrieve as many attributes as requested (reached the end of the enumeration).

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

The caller allocates the array of <a href="/previous-versions/windows/desktop/api/sbe/ns-sbe-streambuffer_attribute">STREAMBUFFER_ATTRIBUTE</a> structures, but the method allocates buffers for the attributes and the attribute names, which are contained in the <b>pszName</b> and <b>pbAttribute</b> members of each structure. The caller must release those buffers, by calling <b>CoTaskMemFree</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-ienumstreambufferrecordingattrib">IEnumStreamBufferRecordingAttrib Interface</a>