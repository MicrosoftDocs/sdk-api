---
UID: NF:namespaceapi.DeleteBoundaryDescriptor
title: DeleteBoundaryDescriptor function (namespaceapi.h)
author: windows-sdk-content
description: Deletes the specified boundary descriptor.
old-location: base\deleteboundarydescriptor.htm
tech.root: Sync
ms.assetid: 759d9cd9-9ef2-4bbe-9e99-8aec87f5ba4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteBoundaryDescriptor, DeleteBoundaryDescriptor function, base.deleteboundarydescriptor, namespaceapi/DeleteBoundaryDescriptor, winbase/DeleteBoundaryDescriptor
ms.topic: function
req.header: namespaceapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Namespace-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - DeleteBoundaryDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteBoundaryDescriptor function


## -description


Deletes the specified boundary descriptor.


## -parameters




### -param BoundaryDescriptor [in]

A handle to the boundary descriptor. The <a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a> function returns this handle.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a>



<a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>
 

 

