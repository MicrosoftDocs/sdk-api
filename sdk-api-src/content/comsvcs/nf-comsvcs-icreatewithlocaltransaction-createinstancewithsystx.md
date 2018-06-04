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

# ICreateWithLocalTransaction::CreateInstanceWithSysTx


## -description


Creates a COM+ object that executes within the scope of the specified local transaction.


## -parameters




### -param pTransaction [in]

The transaction in which the requested object participates.


### -param rclsid [in]

The CLSID of the class from which to create the requested object.


### -param riid [in]

A reference to the interface identifier (IID) of the interface that is used to communicate with the request object.


### -param pObject [out, retval]

The address of the pointer variable that receives the interface pointer specified with <i>riid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/667ebc77-943c-4cf0-90b4-7c28949f406e">ICreateWithLocalTransaction</a>
 

 

