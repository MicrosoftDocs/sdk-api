---
UID: NF:sbe.IStreamBufferRecordingAttribute.EnumAttributes
title: IStreamBufferRecordingAttribute::EnumAttributes (sbe.h)
description: The EnumAttributes method enumerates the existing attributes of the stream buffer file. This method returns an enumerator object, which the caller can then use to enumerate the attributes.
helpviewer_keywords: ["EnumAttributes","EnumAttributes method [Microsoft TV Technologies]","EnumAttributes method [Microsoft TV Technologies]","IStreamBufferRecordingAttribute interface","IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","EnumAttributes method","IStreamBufferRecordingAttribute.EnumAttributes","IStreamBufferRecordingAttribute::EnumAttributes","IStreamBufferRecordingAttributeEnumAttributes","mstv.istreambufferrecordingattribute_enumattributes","sbe/IStreamBufferRecordingAttribute::EnumAttributes"]
old-location: mstv\istreambufferrecordingattribute_enumattributes.htm
tech.root: mstv
ms.assetid: 2944d1c4-a4ed-47a7-a0c4-a75cddb9cc99
ms.date: 12/05/2018
ms.keywords: EnumAttributes, EnumAttributes method [Microsoft TV Technologies], EnumAttributes method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],EnumAttributes method, IStreamBufferRecordingAttribute.EnumAttributes, IStreamBufferRecordingAttribute::EnumAttributes, IStreamBufferRecordingAttributeEnumAttributes, mstv.istreambufferrecordingattribute_enumattributes, sbe/IStreamBufferRecordingAttribute::EnumAttributes
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
 - IStreamBufferRecordingAttribute::EnumAttributes
 - sbe/IStreamBufferRecordingAttribute::EnumAttributes
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
 - IStreamBufferRecordingAttribute.EnumAttributes
---

# IStreamBufferRecordingAttribute::EnumAttributes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>EnumAttributes</b> method enumerates the existing attributes of the stream buffer file. This method returns an enumerator object, which the caller can then use to enumerate the attributes.

## -parameters

### -param ppIEnumStreamBufferAttrib [out]

Receives an <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-ienumstreambufferrecordingattrib">IEnumStreamBufferRecordingAttrib</a> interface pointer.
          The caller must release the interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
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