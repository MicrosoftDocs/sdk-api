---
UID: NF:mfobjects.IMFCollection.GetElementCount
title: IMFCollection::GetElementCount (mfobjects.h)
description: Retrieves the number of objects in the collection. (IMFCollection.GetElementCount)
helpviewer_keywords: ["4bd46f66-0542-4185-b50e-163cc3b4e2f8","GetElementCount","GetElementCount method [Media Foundation]","GetElementCount method [Media Foundation]","IMFCollection interface","IMFCollection interface [Media Foundation]","GetElementCount method","IMFCollection.GetElementCount","IMFCollection::GetElementCount","mf.imfcollection_getelementcount","mfobjects/IMFCollection::GetElementCount"]
old-location: mf\imfcollection_getelementcount.htm
tech.root: mf
ms.assetid: 4bd46f66-0542-4185-b50e-163cc3b4e2f8
ms.date: 12/05/2018
ms.keywords: 4bd46f66-0542-4185-b50e-163cc3b4e2f8, GetElementCount, GetElementCount method [Media Foundation], GetElementCount method [Media Foundation],IMFCollection interface, IMFCollection interface [Media Foundation],GetElementCount method, IMFCollection.GetElementCount, IMFCollection::GetElementCount, mf.imfcollection_getelementcount, mfobjects/IMFCollection::GetElementCount
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCollection::GetElementCount
 - mfobjects/IMFCollection::GetElementCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFCollection.GetElementCount
---

# IMFCollection::GetElementCount


## -description

Retrieves the number of objects in the collection.

## -parameters

### -param pcElements [out]

Receives the number of objects in the collection.

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

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a>
