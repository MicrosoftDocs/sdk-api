---
UID: NF:mfobjects.IMFCollection.GetElement
title: IMFCollection::GetElement (mfobjects.h)
description: Retrieves an object in the collection.
helpviewer_keywords: ["GetElement","GetElement method [Media Foundation]","GetElement method [Media Foundation]","IMFCollection interface","IMFCollection interface [Media Foundation]","GetElement method","IMFCollection.GetElement","IMFCollection::GetElement","a45983a8-4061-40e1-a11a-67de0867e553","mf.imfcollection_getelement","mfobjects/IMFCollection::GetElement"]
old-location: mf\imfcollection_getelement.htm
tech.root: mf
ms.assetid: a45983a8-4061-40e1-a11a-67de0867e553
ms.date: 12/05/2018
ms.keywords: GetElement, GetElement method [Media Foundation], GetElement method [Media Foundation],IMFCollection interface, IMFCollection interface [Media Foundation],GetElement method, IMFCollection.GetElement, IMFCollection::GetElement, a45983a8-4061-40e1-a11a-67de0867e553, mf.imfcollection_getelement, mfobjects/IMFCollection::GetElement
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
 - IMFCollection::GetElement
 - mfobjects/IMFCollection::GetElement
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
 - IMFCollection.GetElement
---

# IMFCollection::GetElement


## -description

Retrieves an object in the collection.

## -parameters

### -param dwElementIndex [in]

Zero-based index of the object to retrieve. Objects are indexed in the order in which they were added to the collection.

### -param ppUnkElement [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface. The retrieved pointer value might be <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not remove the object from the collection. To remove an object, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-removeelement">IMFCollection::RemoveElement</a>.
      


#### Examples


```cpp
//  Gets an interface pointer from a collection (IMFCollection).
//
//  Q: Interface type

template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, 
    DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a>