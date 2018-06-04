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

# IWbemObjectAccess::ReadQWORD


## -description


The <b>ReadQWORD</b> method reads 64 bits of property data identified by a property handle.


## -parameters




### -param lHandle [in]

Integer that contains the handle identifying the property.


### -param pqw [out]

Pointer to a unsigned 64-bit integer used to return the data being read.


## -returns



This method returns <b>WBEM_S_NO_ERROR</b> if successful. If the property was <b>NULL</b>, then the method returns <b>WBEM_S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

