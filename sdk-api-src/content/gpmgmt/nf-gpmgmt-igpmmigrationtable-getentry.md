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

# IGPMMigrationTable::GetEntry


## -description


The <b>GetEntry</b> method gets the entry in the migration table for a specified source field.


## -parameters




### -param bstrSource [in]

Source field of the entry to retrieve.


### -param ppEntry [out]

A pointer to an <a href="https://msdn.microsoft.com/85a9bebf-0d96-4ec1-a0bf-37b262059067">IGPMMapEntry</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/85a9bebf-0d96-4ec1-a0bf-37b262059067">GPMMapEntry</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/85a9bebf-0d96-4ec1-a0bf-37b262059067">GPMMapEntry</a> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

