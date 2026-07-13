---
UID: NF:wuapi.IStringCollection.Insert
title: IStringCollection::Insert (wuapi.h)
description: Inserts an item into the collection at the specified position. (IStringCollection.Insert)
helpviewer_keywords: ["IStringCollection interface [Windows Update Agent]","Insert method","IStringCollection.Insert","IStringCollection::Insert","Insert","Insert method [Windows Update Agent]","Insert method [Windows Update Agent]","IStringCollection interface","wua.istringcollection_insert","wuapi/IStringCollection::Insert"]
old-location: wua\istringcollection_insert.htm
tech.root: wua
ms.assetid: 51a00dde-7781-4674-bbb2-10bb2eb23548
ms.date: 12/05/2018
ms.keywords: IStringCollection interface [Windows Update Agent],Insert method, IStringCollection.Insert, IStringCollection::Insert, Insert, Insert method [Windows Update Agent], Insert method [Windows Update Agent],IStringCollection interface, wua.istringcollection_insert, wuapi/IStringCollection::Insert
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStringCollection::Insert
 - wuapi/IStringCollection::Insert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IStringCollection.Insert
---

# IStringCollection::Insert


## -description

Inserts an item into the collection at the specified position.

## -parameters

### -param index [in]

The position at which a new string is inserted.

### -param value [in]

The string to be inserted.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
An index is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a>
