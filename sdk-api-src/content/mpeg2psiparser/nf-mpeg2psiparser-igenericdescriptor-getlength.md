---
UID: NF:mpeg2psiparser.IGenericDescriptor.GetLength
title: IGenericDescriptor::GetLength (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IGenericDescriptor interface","IGenericDescriptor interface [Microsoft TV Technologies]","GetLength method","IGenericDescriptor.GetLength","IGenericDescriptor::GetLength","IGenericDescriptorGetLength","mpeg2psiparser/IGenericDescriptor::GetLength","mstv.igenericdescriptor_getlength"]
old-location: mstv\igenericdescriptor_getlength.htm
tech.root: mstv
ms.assetid: fd36bb87-ef30-4064-a251-c89a878eeae9
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IGenericDescriptor interface, IGenericDescriptor interface [Microsoft TV Technologies],GetLength method, IGenericDescriptor.GetLength, IGenericDescriptor::GetLength, IGenericDescriptorGetLength, mpeg2psiparser/IGenericDescriptor::GetLength, mstv.igenericdescriptor_getlength
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
 - IGenericDescriptor::GetLength
 - mpeg2psiparser/IGenericDescriptor::GetLength
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
 - IGenericDescriptor.GetLength
---

# IGenericDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetLength</b> method returns the length of the descriptor body.

## -parameters

### -param pbVal [out]

Receives the length, in bytes.

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