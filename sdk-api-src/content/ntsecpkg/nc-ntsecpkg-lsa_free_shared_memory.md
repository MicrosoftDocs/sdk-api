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

# LSA_FREE_SHARED_MEMORY callback function


## -description


The <b>FreeSharedMemory</b> function frees a block of shared memory previously allocated by the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function.


## -parameters




### -param SharedMem [in]

Pointer to the shared memory section previously reserved using the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function.


### -param Memory [in]

Pointer to the memory previously allocated from the shared memory section specified by the <i>SharedMem</i> parameter, using the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function.


## -returns



This function does not return a value.




## -remarks



A pointer to the <b>FreeSharedMemory</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a>



<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

