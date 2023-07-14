---
UID: NF:sbe.IStreamBufferRecordingAttribute.GetAttributeCount
title: IStreamBufferRecordingAttribute::GetAttributeCount (sbe.h)
description: The GetAttributeCount method returns the number of attributes that are currently defined for this stream buffer file.
helpviewer_keywords: ["GetAttributeCount","GetAttributeCount method [Microsoft TV Technologies]","GetAttributeCount method [Microsoft TV Technologies]","IStreamBufferRecordingAttribute interface","IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","GetAttributeCount method","IStreamBufferRecordingAttribute.GetAttributeCount","IStreamBufferRecordingAttribute::GetAttributeCount","IStreamBufferRecordingAttributeGetAttributeCount","mstv.istreambufferrecordingattribute_getattributecount","sbe/IStreamBufferRecordingAttribute::GetAttributeCount"]
old-location: mstv\istreambufferrecordingattribute_getattributecount.htm
tech.root: mstv
ms.assetid: 44ff4991-f6f2-4f70-bdf5-b8e1dc06611c
ms.date: 12/05/2018
ms.keywords: GetAttributeCount, GetAttributeCount method [Microsoft TV Technologies], GetAttributeCount method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],GetAttributeCount method, IStreamBufferRecordingAttribute.GetAttributeCount, IStreamBufferRecordingAttribute::GetAttributeCount, IStreamBufferRecordingAttributeGetAttributeCount, mstv.istreambufferrecordingattribute_getattributecount, sbe/IStreamBufferRecordingAttribute::GetAttributeCount
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
 - IStreamBufferRecordingAttribute::GetAttributeCount
 - sbe/IStreamBufferRecordingAttribute::GetAttributeCount
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
 - IStreamBufferRecordingAttribute.GetAttributeCount
---

# IStreamBufferRecordingAttribute::GetAttributeCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetAttributeCount</b> method returns the number of attributes that are currently defined for this stream buffer file.

## -parameters

### -param ulReserved [in]

Reserved. Set this parameter to zero.

### -param pcAttributes [out]

Pointer to a variable that receives the number of attributes.

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
NULL pointer argument

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

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordingattribute">IStreamBufferRecordingAttribute Interface</a>