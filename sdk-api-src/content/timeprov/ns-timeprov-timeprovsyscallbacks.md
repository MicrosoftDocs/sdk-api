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

# TimeProvSysCallbacks structure


## -description


Contains pointers to functions for use by the time provider.


## -struct-fields




### -field dwSize

The size of the structure, in bytes.


### -field pfnGetTimeSysInfo

A pointer to the 
<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a> function.


### -field pfnLogTimeProvEvent

A pointer to the 
<a href="https://msdn.microsoft.com/ddaea389-3f58-4011-bcf8-c60546d1bce1">LogTimeProvEventFunc</a> function.


### -field pfnAlertSamplesAvail

A pointer to the 
<a href="https://msdn.microsoft.com/f90da019-072e-46c9-8e05-0321a9960968">AlertSamplesAvailFunc</a> function.


### -field pfnSetProviderStatus

A pointer to the 
<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a> function.


## -see-also




<a href="https://msdn.microsoft.com/f90da019-072e-46c9-8e05-0321a9960968">AlertSamplesAvailFunc</a>



<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a>



<a href="https://msdn.microsoft.com/ddaea389-3f58-4011-bcf8-c60546d1bce1">LogTimeProvEventFunc</a>



<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a>



<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a>
 

 

