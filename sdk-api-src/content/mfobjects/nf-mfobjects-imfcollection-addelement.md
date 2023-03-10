---
UID: NF:mfobjects.IMFCollection.AddElement
title: IMFCollection::AddElement (mfobjects.h)
description: Adds an object to the collection. (IMFCollection.AddElement)
helpviewer_keywords: ["1ef2463b-3d5e-4ed0-ab7c-68758e6cc056","AddElement","AddElement method [Media Foundation]","AddElement method [Media Foundation]","IMFCollection interface","IMFCollection interface [Media Foundation]","AddElement method","IMFCollection.AddElement","IMFCollection::AddElement","mf.imfcollection_addelement","mfobjects/IMFCollection::AddElement"]
old-location: mf\imfcollection_addelement.htm
tech.root: mf
ms.assetid: 1ef2463b-3d5e-4ed0-ab7c-68758e6cc056
ms.date: 12/05/2018
ms.keywords: 1ef2463b-3d5e-4ed0-ab7c-68758e6cc056, AddElement, AddElement method [Media Foundation], AddElement method [Media Foundation],IMFCollection interface, IMFCollection interface [Media Foundation],AddElement method, IMFCollection.AddElement, IMFCollection::AddElement, mf.imfcollection_addelement, mfobjects/IMFCollection::AddElement
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
 - IMFCollection::AddElement
 - mfobjects/IMFCollection::AddElement
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
 - IMFCollection.AddElement
---

# IMFCollection::AddElement


## -description

Adds an object to the collection.

## -parameters

### -param pUnkElement [in]

Pointer to the object's <b>IUnknown</b> interface.

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

## -remarks

If <i>pUnkElement</i> is <b>NULL</b>, a <b>NULL</b> pointer is added to the collection.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a>
