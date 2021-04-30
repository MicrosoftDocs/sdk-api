---
UID: NF:mpeg2data.ISectionList.GetTableIdentifier
title: ISectionList::GetTableIdentifier (mpeg2data.h)
description: The GetTableIdentifier method returns the table identifier (TID) of the packets that this object is receiving.
helpviewer_keywords: ["GetTableIdentifier","GetTableIdentifier method [Microsoft TV Technologies]","GetTableIdentifier method [Microsoft TV Technologies]","ISectionList interface","ISectionList interface [Microsoft TV Technologies]","GetTableIdentifier method","ISectionList.GetTableIdentifier","ISectionList::GetTableIdentifier","ISectionListGetTableIdentifier","mpeg2data/ISectionList::GetTableIdentifier","mstv.isectionlist_gettableidentifier"]
old-location: mstv\isectionlist_gettableidentifier.htm
tech.root: mstv
ms.assetid: e0fd82ec-283e-4d6f-aa74-c65f15df651f
ms.date: 12/05/2018
ms.keywords: GetTableIdentifier, GetTableIdentifier method [Microsoft TV Technologies], GetTableIdentifier method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetTableIdentifier method, ISectionList.GetTableIdentifier, ISectionList::GetTableIdentifier, ISectionListGetTableIdentifier, mpeg2data/ISectionList::GetTableIdentifier, mstv.isectionlist_gettableidentifier
req.header: mpeg2data.h
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
 - ISectionList::GetTableIdentifier
 - mpeg2data/ISectionList::GetTableIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.GetTableIdentifier
---

# ISectionList::GetTableIdentifier


## -description

The <b>GetTableIdentifier</b> method returns the table identifier (TID) of the packets that this object is receiving.

## -parameters

### -param pTableId

Receives the TID.

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

## -remarks

The TID value is set when the object is first initialized.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList Interface</a>