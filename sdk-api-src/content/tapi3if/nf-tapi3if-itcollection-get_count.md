---
UID: NF:tapi3if.ITCollection.get_Count
title: ITCollection::get_Count (tapi3if.h)
description: The get_Count method gets the number of items in the collection.
helpviewer_keywords: ["ITCollection interface [TAPI 2.2]","get_Count method","ITCollection.get_Count","ITCollection::get_Count","_tapi3_itcollection_get_count","get_Count","get_Count method [TAPI 2.2]","get_Count method [TAPI 2.2]","ITCollection interface","tapi3.itcollection_get_count","tapi3if/ITCollection::get_Count"]
old-location: tapi3\itcollection_get_count.htm
tech.root: tapi3
ms.assetid: 253c09db-4b64-43d0-8040-b3a2ab95af30
ms.date: 12/05/2018
ms.keywords: ITCollection interface [TAPI 2.2],get_Count method, ITCollection.get_Count, ITCollection::get_Count, _tapi3_itcollection_get_count, get_Count, get_Count method [TAPI 2.2], get_Count method [TAPI 2.2],ITCollection interface, tapi3.itcollection_get_count, tapi3if/ITCollection::get_Count
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCollection::get_Count
 - tapi3if/ITCollection::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCollection.get_Count
---

# ITCollection::get_Count


## -description

The 
<b>get_Count</b> method gets the number of items in the collection.

## -parameters

### -param lCount [out]

Number of items.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>