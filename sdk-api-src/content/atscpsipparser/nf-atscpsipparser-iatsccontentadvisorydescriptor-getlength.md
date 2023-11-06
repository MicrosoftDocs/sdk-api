---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetLength
title: IAtscContentAdvisoryDescriptor::GetLength (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IAtscContentAdvisoryDescriptor interface","IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies]","GetLength method","IAtscContentAdvisoryDescriptor.GetLength","IAtscContentAdvisoryDescriptor::GetLength","IAtscContentAdvisoryDescriptorGetLength","atscpsipparser/IAtscContentAdvisoryDescriptor::GetLength","mstv.iatsccontentadvisorydescriptor_getlength"]
old-location: mstv\iatsccontentadvisorydescriptor_getlength.htm
tech.root: mstv
ms.assetid: 954d7dc4-43dd-4e33-a3cf-7584092cd0e7
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetLength method, IAtscContentAdvisoryDescriptor.GetLength, IAtscContentAdvisoryDescriptor::GetLength, IAtscContentAdvisoryDescriptorGetLength, atscpsipparser/IAtscContentAdvisoryDescriptor::GetLength, mstv.iatsccontentadvisorydescriptor_getlength
req.header: atscpsipparser.h
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
 - IAtscContentAdvisoryDescriptor::GetLength
 - atscpsipparser/IAtscContentAdvisoryDescriptor::GetLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetLength
---

# IAtscContentAdvisoryDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetLength</b> method returns the length of the descriptor body.

## -parameters

### -param pbVal [out]

Receives the length of the descriptor body, in bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsccontentadvisorydescriptor">IAtscContentAdvisoryDescriptor Interface</a>