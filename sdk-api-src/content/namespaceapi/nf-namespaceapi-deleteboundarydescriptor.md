---
UID: NF:namespaceapi.DeleteBoundaryDescriptor
title: DeleteBoundaryDescriptor function (namespaceapi.h)
author: windows-sdk-content
description: Deletes the specified boundary descriptor.
old-location: base\deleteboundarydescriptor.htm
tech.root: Sync
ms.assetid: 759d9cd9-9ef2-4bbe-9e99-8aec87f5ba4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteBoundaryDescriptor, DeleteBoundaryDescriptor function, base.deleteboundarydescriptor, namespaceapi/DeleteBoundaryDescriptor, winbase/DeleteBoundaryDescriptor
ms.topic: function
f1_keywords: 
 - "namespaceapi/DeleteBoundaryDescriptor"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteBoundaryDescriptor function


## -description


Deletes the specified boundary descriptor.


## -parameters




### -param BoundaryDescriptor [in]

A handle to the boundary descriptor. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a> function returns this handle.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>
 

 

