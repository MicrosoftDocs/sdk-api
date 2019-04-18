---
UID: NF:winbase.CreateBoundaryDescriptorA
title: CreateBoundaryDescriptorA function (winbase.h)
author: windows-sdk-content
description: Creates a boundary descriptor.
old-location: base\createboundarydescriptor.htm
tech.root: Sync
ms.assetid: c7789e90-8dfb-47ee-a0b2-906520982d84
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBoundaryDescriptor, CreateBoundaryDescriptor function, CreateBoundaryDescriptorA, CreateBoundaryDescriptorW, base.createboundarydescriptor, winbase/CreateBoundaryDescriptor, winbase/CreateBoundaryDescriptorA, winbase/CreateBoundaryDescriptorW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateBoundaryDescriptorW (Unicode) and CreateBoundaryDescriptorA (ANSI)
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
 - API-Ms-Win-Core-Namespace-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CreateBoundaryDescriptor
 - CreateBoundaryDescriptorA
 - CreateBoundaryDescriptorW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

