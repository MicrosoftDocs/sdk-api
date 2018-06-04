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

# CreateBoundaryDescriptorA function


## -description


Creates a boundary descriptor.


## -parameters




### -param Name [in]

The name of the boundary descriptor.


### -param Flags [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is a handle to the boundary descriptor.


       If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
     




## -remarks



A new boundary descriptor must have at least one security identifier (SID). To add a SID to a boundary descriptor, use the <a href="https://msdn.microsoft.com/c0dd01a0-1a08-43dc-8cef-dff290e73ca1">AddSIDToBoundaryDescriptor</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/c0dd01a0-1a08-43dc-8cef-dff290e73ca1">AddSIDToBoundaryDescriptor</a>



<a href="https://msdn.microsoft.com/bb6331b0-88cb-4695-b159-6e8750440a69">CreatePrivateNamespace</a>



<a href="https://msdn.microsoft.com/759d9cd9-9ef2-4bbe-9e99-8aec87f5ba4a">DeleteBoundaryDescriptor</a>



<a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>
 

 

