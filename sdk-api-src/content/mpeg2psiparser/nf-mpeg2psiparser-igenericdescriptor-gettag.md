---
UID: NF:mpeg2psiparser.IGenericDescriptor.GetTag
title: IGenericDescriptor::GetTag (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IGenericDescriptor interface","IGenericDescriptor interface [Microsoft TV Technologies]","GetTag method","IGenericDescriptor.GetTag","IGenericDescriptor::GetTag","IGenericDescriptorGetTag","mpeg2psiparser/IGenericDescriptor::GetTag","mstv.igenericdescriptor_gettag"]
old-location: mstv\igenericdescriptor_gettag.htm
tech.root: mstv
ms.assetid: b8923e91-46e1-48fa-a24c-d43cc4a09bd2
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IGenericDescriptor interface, IGenericDescriptor interface [Microsoft TV Technologies],GetTag method, IGenericDescriptor.GetTag, IGenericDescriptor::GetTag, IGenericDescriptorGetTag, mpeg2psiparser/IGenericDescriptor::GetTag, mstv.igenericdescriptor_gettag
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
 - IGenericDescriptor::GetTag
 - mpeg2psiparser/IGenericDescriptor::GetTag
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
 - IGenericDescriptor.GetTag
---

# IGenericDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetTag</b> method returns the descriptor tag.

## -parameters

### -param pbVal [out]

Receives the tag.

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