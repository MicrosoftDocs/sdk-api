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

# ICertExit2::GetManageModule


## -description


The <b>GetManageModule</b> method retrieves the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface by calling <b>GetManageModule</b> and passing in the address of a pointer to an <b>ICertManageModule</b>.


## -parameters




### -param ppManageModule [out]

Pointer to the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The return value is a <b>Variant</b> containing the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface.



