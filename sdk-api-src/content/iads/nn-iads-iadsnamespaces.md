---
UID: NN:iads.IADsNamespaces
title: IADsNamespaces (iads.h)
description: The IADsNamespaces interface is implemented by the ADs provider and is used for managing namespace objects.
helpviewer_keywords: ["IADsNamespaces","IADsNamespaces interface [ADSI]","IADsNamespaces interface [ADSI]","described","_ds_iadsnamespaces","adsi.iadsnamespaces","iads/IADsNamespaces"]
old-location: adsi\iadsnamespaces.htm
tech.root: adsi
ms.assetid: edac671e-9ab1-4211-9fd7-1a0b965196b4
ms.date: 12/05/2018
ms.keywords: IADsNamespaces, IADsNamespaces interface [ADSI], IADsNamespaces interface [ADSI],described, _ds_iadsnamespaces, adsi.iadsnamespaces, iads/IADsNamespaces
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsNamespaces
 - iads/IADsNamespaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsNamespaces
---

# IADsNamespaces interface


## -description

The <b>IADsNamespaces</b> interface is implemented by the ADs provider and is used for managing namespace objects. A namespace object is a provider-specific top-level container and corresponds to the root node of a directory tree. The ADSI namespaces object serves as an entry point into the underlying directory and allows directory service administrators to enumerate the currently installed namespace objects.

This interface supports two property methods to get and set the <a href="/windows/desktop/ADSI/iadsnamespaces-property-methods">DefaultContainer</a> property which holds the path to a container object. The default container is the base node from which browsing of the directory tree proceeds. References of any children objects can be made relative to this default container. The <b>DefaultContainer</b> property makes it more efficient and convenient for a client to reference repetitively a contained object.

Obtain a pointer to the <b>IADsNamespaces</b> interface when you bind to the object using the "ADs:" string:

```vb
Dim ns As IADsNamespaces
Set ns = GetObject("ADs:")
```

Non-Automation clients can use the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a> helper function instead.

```cpp
IADsNamespaces *pNs;
hr = ADsGetObject(L"ADs:", IID_IADsNamespaces, (void**)&pNs);
```

In addition to the <b>IADsNamespaces</b> interface, the ADSI namespaces object also implements the <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface.

## -see-also

<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a>



<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>