---
UID: NF:namespaceapi.AddSIDToBoundaryDescriptor
title: AddSIDToBoundaryDescriptor function (namespaceapi.h)
author: windows-sdk-content
description: Adds a security identifier (SID) to the specified boundary descriptor.
old-location: base\addsidtoboundarydescriptor.htm
tech.root: Sync
ms.assetid: c0dd01a0-1a08-43dc-8cef-dff290e73ca1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddSIDToBoundaryDescriptor, AddSIDToBoundaryDescriptor function, base.addsidtoboundarydescriptor, namespaceapi/AddSIDToBoundaryDescriptor, winbase/AddSIDToBoundaryDescriptor
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
 - AddSIDToBoundaryDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddSIDToBoundaryDescriptor function


## -description


Adds a security identifier (SID) to the specified boundary descriptor.


## -parameters




### -param BoundaryDescriptor [in, out]

A handle to the boundary descriptor. The <a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a> function returns this handle.


### -param RequiredSid [in]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>AddSIDToBoundaryDescriptor</b> function must be called once for each SID to be added to the boundary descriptor.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a>



<a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>
 

 

