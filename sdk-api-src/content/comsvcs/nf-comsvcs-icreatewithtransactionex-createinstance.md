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

# ICreateWithTransactionEx::CreateInstance


## -description


Creates a COM+ object that executes within the scope of a manual transaction specified with a reference to an <b>ITransaction</b> interface.


## -parameters




### -param pTransaction [in]

An <b>ITransaction</b> interface pointer indicating the transaction in which you want to create the COM+ object.


### -param rclsid [in]

The CLSID of the type of object to instantiate.


### -param riid [in]

The ID of the interface to be returned by the <i>ppvObj</i> parameter.


### -param pObject [out]

A new object of the type specified by the <i>rclsid</i> argument through the interface specified by the <i>riid</i> argument.


## -returns



This method can return the following values:




## -see-also




<a href="https://msdn.microsoft.com/39b455d3-d3d2-46ae-a45e-b036c18e45bc">ICreateWithTransactionEx</a>
 

 

