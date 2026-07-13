---
UID: NF:mpeg2psiparser.IGenericDescriptor.Initialize
title: IGenericDescriptor::Initialize (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IGenericDescriptor interface [Microsoft TV Technologies]","Initialize method","IGenericDescriptor.Initialize","IGenericDescriptor::Initialize","IGenericDescriptorInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IGenericDescriptor interface","mpeg2psiparser/IGenericDescriptor::Initialize","mstv.igenericdescriptor_initialize"]
old-location: mstv\igenericdescriptor_initialize.htm
tech.root: mstv
ms.assetid: 0dfe1f52-60ac-46b6-9f55-9764b47479e8
ms.date: 12/05/2018
ms.keywords: IGenericDescriptor interface [Microsoft TV Technologies],Initialize method, IGenericDescriptor.Initialize, IGenericDescriptor::Initialize, IGenericDescriptorInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IGenericDescriptor interface, mpeg2psiparser/IGenericDescriptor::Initialize, mstv.igenericdescriptor_initialize
req.header: mpeg2psiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IGenericDescriptor::Initialize
 - mpeg2psiparser/IGenericDescriptor::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IGenericDescriptor.Initialize
---

# IGenericDescriptor::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>Initialize</b> method initializes the object. This method is called internally by the various methods that return <b>IGenericDescriptor</b> interface pointers, so applications typically should not call it.

## -parameters

### -param pbDesc [in]

Pointer to a buffer that contains the raw descriptor data.

### -param bCount [in]

Specifies the size of the buffer, in bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid or malformed descriptor.

</td>
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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor Interface</a>