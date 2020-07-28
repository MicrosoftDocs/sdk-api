---
UID: NF:winbase.CreateBoundaryDescriptorA
title: CreateBoundaryDescriptorA function (winbase.h)
description: Creates a boundary descriptor.
helpviewer_keywords: ["CreateBoundaryDescriptor","CreateBoundaryDescriptor function","CreateBoundaryDescriptorA","CreateBoundaryDescriptorW","base.createboundarydescriptor","winbase/CreateBoundaryDescriptor","winbase/CreateBoundaryDescriptorA","winbase/CreateBoundaryDescriptorW"]
old-location: base\createboundarydescriptor.htm
tech.root: backup
ms.assetid: c7789e90-8dfb-47ee-a0b2-906520982d84
ms.date: 12/05/2018
ms.keywords: CreateBoundaryDescriptor, CreateBoundaryDescriptor function, CreateBoundaryDescriptorA, CreateBoundaryDescriptorW, base.createboundarydescriptor, winbase/CreateBoundaryDescriptor, winbase/CreateBoundaryDescriptorA, winbase/CreateBoundaryDescriptorW
f1_keywords:
- winbase/CreateBoundaryDescriptor
dev_langs:
- c++
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
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
     




## -remarks



A new boundary descriptor must have at least one security identifier (SID). To add a SID to a boundary descriptor, use the <a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor">AddSIDToBoundaryDescriptor</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor">AddSIDToBoundaryDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprivatenamespacea">CreatePrivateNamespace</a>



<a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-deleteboundarydescriptor">DeleteBoundaryDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>
 

 

