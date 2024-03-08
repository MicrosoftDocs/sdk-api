---
UID: NF:wuapi.IStringCollection.Add
title: IStringCollection::Add (wuapi.h)
description: Adds an item to the collection. (IStringCollection.Add)
helpviewer_keywords: ["Add","Add method [Windows Update Agent]","Add method [Windows Update Agent]","IStringCollection interface","IStringCollection interface [Windows Update Agent]","Add method","IStringCollection.Add","IStringCollection::Add","wua.istringcollection_add","wuapi/IStringCollection::Add"]
old-location: wua\istringcollection_add.htm
tech.root: wua
ms.assetid: f5412e0d-a8b7-43a6-b7a5-95d662459f78
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Update Agent], Add method [Windows Update Agent],IStringCollection interface, IStringCollection interface [Windows Update Agent],Add method, IStringCollection.Add, IStringCollection::Add, wua.istringcollection_add, wuapi/IStringCollection::Add
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
 - IStringCollection::Add
 - wuapi/IStringCollection::Add
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
 - IStringCollection.Add
---

# IStringCollection::Add


## -description

Adds an item to the collection.

## -parameters

### -param value [in]

A string to be added to the collection.

### -param retval [out]

The index of the added interface in the collection.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
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
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a>
