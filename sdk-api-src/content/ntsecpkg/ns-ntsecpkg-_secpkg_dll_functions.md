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

# _SECPKG_DLL_FUNCTIONS structure


## -description


The <b>SECPKG_DLL_FUNCTIONS</b> structure contains pointers to the LSA functions that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> can call while executing in-process with a client/server application. The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) provides this structure during user-mode initialization using each security package's 
<a href="https://msdn.microsoft.com/12f5903d-af13-40fd-8a23-2a28ffd9fc44">SpInstanceInit</a> function.


## -struct-fields




### -field AllocateHeap

Pointer to the  <a href="https://msdn.microsoft.com/8e97ea0e-42f5-4641-83d7-3858c533479c">AllocateHeap</a> function.
					


### -field FreeHeap

Pointer to the  <a href="https://msdn.microsoft.com/9aa28a2f-c71d-4f82-bc14-257ed51b9c88">FreeHeap</a> function.
					


### -field RegisterCallback

Pointer to the  <a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a> function.
					


### -field LocatePackageById

 



