---
UID: NF:namespaceapi.AddSIDToBoundaryDescriptor
title: AddSIDToBoundaryDescriptor function (namespaceapi.h)
description: Adds a security identifier (SID) to the specified boundary descriptor.helpviewer_keywords: ["AddSIDToBoundaryDescriptor","AddSIDToBoundaryDescriptor function","base.addsidtoboundarydescriptor","namespaceapi/AddSIDToBoundaryDescriptor","winbase/AddSIDToBoundaryDescriptor"]
old-location: base\addsidtoboundarydescriptor.htm
tech.root: Sync
ms.assetid: c0dd01a0-1a08-43dc-8cef-dff290e73ca1
ms.date: 12/05/2018
ms.keywords: AddSIDToBoundaryDescriptor, AddSIDToBoundaryDescriptor function, base.addsidtoboundarydescriptor, namespaceapi/AddSIDToBoundaryDescriptor, winbase/AddSIDToBoundaryDescriptor
f1_keywords:
- namespaceapi/AddSIDToBoundaryDescriptor
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
- AddSIDToBoundaryDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddSIDToBoundaryDescriptor function


## -description


Adds a security identifier (SID) to the specified boundary descriptor.


## -parameters




### -param BoundaryDescriptor [in, out]

A handle to the boundary descriptor. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a> function returns this handle.


### -param RequiredSid [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>AddSIDToBoundaryDescriptor</b> function must be called once for each SID to be added to the boundary descriptor.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>
 

 

