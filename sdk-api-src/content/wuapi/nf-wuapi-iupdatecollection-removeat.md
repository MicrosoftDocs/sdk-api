---
UID: NF:wuapi.IUpdateCollection.RemoveAt
title: IUpdateCollection::RemoveAt (wuapi.h)
description: Removes the item at the specified index from the collection. (IUpdateCollection.RemoveAt)
helpviewer_keywords: ["IUpdateCollection interface [Windows Update Agent]","RemoveAt method","IUpdateCollection.RemoveAt","IUpdateCollection::RemoveAt","RemoveAt","RemoveAt method [Windows Update Agent]","RemoveAt method [Windows Update Agent]","IUpdateCollection interface","wua.iupdatecollection_removeat","wuapi/IUpdateCollection::RemoveAt"]
old-location: wua\iupdatecollection_removeat.htm
tech.root: wua
ms.assetid: b6d32db8-c935-41f8-a8f3-0730719cac7e
ms.date: 12/05/2018
ms.keywords: IUpdateCollection interface [Windows Update Agent],RemoveAt method, IUpdateCollection.RemoveAt, IUpdateCollection::RemoveAt, RemoveAt, RemoveAt method [Windows Update Agent], RemoveAt method [Windows Update Agent],IUpdateCollection interface, wua.iupdatecollection_removeat, wuapi/IUpdateCollection::RemoveAt
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
 - IUpdateCollection::RemoveAt
 - wuapi/IUpdateCollection::RemoveAt
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
 - IUpdateCollection.RemoveAt
---

# IUpdateCollection::RemoveAt


## -description

Removes the item at the specified index from the collection.

## -parameters

### -param index [in]

The index of the interface to be removed.

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

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatecollection">IUpdateCollection</a>
