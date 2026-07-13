---
UID: NF:mpeg2psiparser.ICAT.GetCountOfTableDescriptors
title: ICAT::GetCountOfTableDescriptors (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","ICAT interface","ICAT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","ICAT.GetCountOfTableDescriptors","ICAT::GetCountOfTableDescriptors","ICATGetCountOfTableDescriptors","mpeg2psiparser/ICAT::GetCountOfTableDescriptors","mstv.icat_getcountoftabledescriptors"]
old-location: mstv\icat_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 3111eecc-b869-4235-8af4-cc0ef9cc5e4e
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],ICAT interface, ICAT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, ICAT.GetCountOfTableDescriptors, ICAT::GetCountOfTableDescriptors, ICATGetCountOfTableDescriptors, mpeg2psiparser/ICAT::GetCountOfTableDescriptors, mstv.icat_getcountoftabledescriptors
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
 - ICAT::GetCountOfTableDescriptors
 - mpeg2psiparser/ICAT::GetCountOfTableDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mpeg2psiparser.h
api_name:
 - ICAT.GetCountOfTableDescriptors
---

# ICAT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the CAT.

## -parameters

### -param pdwVal [out]

Receives the number of descriptors.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-icat">ICAT Interface</a>