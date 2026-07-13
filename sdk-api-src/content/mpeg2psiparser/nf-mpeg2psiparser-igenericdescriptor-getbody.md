---
UID: NF:mpeg2psiparser.IGenericDescriptor.GetBody
title: IGenericDescriptor::GetBody (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetBody","GetBody method [Microsoft TV Technologies]","GetBody method [Microsoft TV Technologies]","IGenericDescriptor interface","IGenericDescriptor interface [Microsoft TV Technologies]","GetBody method","IGenericDescriptor.GetBody","IGenericDescriptor::GetBody","IGenericDescriptorGetBody","mpeg2psiparser/IGenericDescriptor::GetBody","mstv.igenericdescriptor_getbody"]
old-location: mstv\igenericdescriptor_getbody.htm
tech.root: mstv
ms.assetid: fbb17e16-b0a4-45c1-b723-cbb6a61d4d0f
ms.date: 12/05/2018
ms.keywords: GetBody, GetBody method [Microsoft TV Technologies], GetBody method [Microsoft TV Technologies],IGenericDescriptor interface, IGenericDescriptor interface [Microsoft TV Technologies],GetBody method, IGenericDescriptor.GetBody, IGenericDescriptor::GetBody, IGenericDescriptorGetBody, mpeg2psiparser/IGenericDescriptor::GetBody, mstv.igenericdescriptor_getbody
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
 - IGenericDescriptor::GetBody
 - mpeg2psiparser/IGenericDescriptor::GetBody
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
 - IGenericDescriptor.GetBody
---

# IGenericDescriptor::GetBody


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetBody</b> method returns the body of the descriptor.

## -parameters

### -param ppbVal [out]

Receives a pointer to a buffer. To get the size of the buffer, call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-igenericdescriptor-getlength">IGenericDescriptor::GetLength</a> method. The buffer contains the body of the descriptor, in network byte order (Big Endian). The caller is responsible for converting the data to Little Endian byte order. The caller must free the buffer by calling the <b>CoTaskMemFree</b> function.

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