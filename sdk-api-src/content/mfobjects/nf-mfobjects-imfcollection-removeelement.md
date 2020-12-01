---
UID: NF:mfobjects.IMFCollection.RemoveElement
title: IMFCollection::RemoveElement (mfobjects.h)
description: Removes an object from the collection.
helpviewer_keywords: ["47f33235-6bb5-4103-82b4-87210b0e695c","IMFCollection interface [Media Foundation]","RemoveElement method","IMFCollection.RemoveElement","IMFCollection::RemoveElement","RemoveElement","RemoveElement method [Media Foundation]","RemoveElement method [Media Foundation]","IMFCollection interface","mf.imfcollection_removeelement","mfobjects/IMFCollection::RemoveElement"]
old-location: mf\imfcollection_removeelement.htm
tech.root: mf
ms.assetid: 47f33235-6bb5-4103-82b4-87210b0e695c
ms.date: 12/05/2018
ms.keywords: 47f33235-6bb5-4103-82b4-87210b0e695c, IMFCollection interface [Media Foundation],RemoveElement method, IMFCollection.RemoveElement, IMFCollection::RemoveElement, RemoveElement, RemoveElement method [Media Foundation], RemoveElement method [Media Foundation],IMFCollection interface, mf.imfcollection_removeelement, mfobjects/IMFCollection::RemoveElement
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
 - IMFCollection::RemoveElement
 - mfobjects/IMFCollection::RemoveElement
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
 - IMFCollection.RemoveElement
---

# IMFCollection::RemoveElement


## -description

Removes an object from the collection.

## -parameters

### -param dwElementIndex [in]

Zero-based index of the object to remove. Objects are indexed in the order in which they were added to the collection.

### -param ppUnkElement [out]

Receives a pointer to the <b>IUnknown</b> interface of the object. The caller must release the interface. This parameter cannot be <b>NULL</b>, but the retrieved pointer value might be <b>NULL</b>.

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