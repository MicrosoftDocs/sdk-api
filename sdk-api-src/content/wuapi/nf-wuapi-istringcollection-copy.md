---
UID: NF:wuapi.IStringCollection.Copy
title: IStringCollection::Copy (wuapi.h)
description: Creates a deep read/write copy of the collection.
helpviewer_keywords: ["Copy","Copy method [Windows Update Agent]","Copy method [Windows Update Agent]","IStringCollection interface","IStringCollection interface [Windows Update Agent]","Copy method","IStringCollection.Copy","IStringCollection::Copy","wua.istringcollection_copy","wuapi/IStringCollection::Copy"]
old-location: wua\istringcollection_copy.htm
tech.root: wua
ms.assetid: e2f6d5c0-c92a-44e5-a322-f336a3ef64ce
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [Windows Update Agent], Copy method [Windows Update Agent],IStringCollection interface, IStringCollection interface [Windows Update Agent],Copy method, IStringCollection.Copy, IStringCollection::Copy, wua.istringcollection_copy, wuapi/IStringCollection::Copy
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
 - IStringCollection::Copy
 - wuapi/IStringCollection::Copy
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
 - IStringCollection.Copy
---

# IStringCollection::Copy


## -description

Creates a deep read/write copy of the collection.

## -parameters

### -param retval [out]

A deep read/write copy of the collection.

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
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a>