---
UID: NN:iads.IADsNamespaces
title: IADsNamespaces
author: windows-sdk-content
description: The IADsNamespaces interface is implemented by the ADs provider and is used for managing namespace objects.
old-location: adsi\iadsnamespaces.htm
tech.root: ADSI
ms.assetid: edac671e-9ab1-4211-9fd7-1a0b965196b4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsNamespaces, IADsNamespaces interface [ADSI], IADsNamespaces interface [ADSI],described, _ds_iadsnamespaces, adsi.iadsnamespaces, iads/IADsNamespaces
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsNamespaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsNamespaces interface


## -description


The <b>IADsNamespaces</b> interface is implemented by the ADs provider and is used for managing namespace objects. A namespace object is a provider-specific top-level container and corresponds to the root node of a directory tree. The ADSI namespaces object serves as an entry point into the underlying directory and allows directory service administrators to enumerate the currently installed namespace objects.

This interface supports two property methods to get and set the <a href="https://msdn.microsoft.com/fe959741-429e-480a-8111-3ebadaf55f77">DefaultContainer</a> property which holds the path to a container object. The default container is the base node from which browsing of the directory tree proceeds. References of any children objects can be made relative to this default container. The <b>DefaultContainer</b> property makes it more efficient and convenient for a client to reference repetitively a contained object.

Obtain a pointer to the <b>IADsNamespaces</b> interface when you bind to the object using the "ADs:" string:

```vb
Dim ns As IADsNamespaces
Set ns = GetObject("ADs:")
```

Non-Automation clients can use the <a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a> helper function instead.

```cpp
IADsNamespaces *pNs;
hr = ADsGetObject(L"ADs:", IID_IADsNamespaces, (void**)&pNs);
```

In addition to the <b>IADsNamespaces</b> interface, the ADSI namespaces object also implements the <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

