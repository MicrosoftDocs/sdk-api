---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICreateObject::CreateObject


## -description


Creates a local object of a specified class and returns a pointer to a specified interface on the object.


## -parameters




### -param clsid [in]

Type: <b>REFCLSID</b>

A reference to a CLSID.


### -param pUnkOuter [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that aggregates the object created by this function, or <b>NULL</b> if no aggregation is desired.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface the created object should return.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the pointer to the interface requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be used with <a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">GetPropertyStoreWithCreateObject</a>.



