---
UID: NF:winbase.CreateBoundaryDescriptorA
title: CreateBoundaryDescriptorA function (winbase.h)
description: The CreateBoundaryDescriptorA (ANSI) function (winbase.h) creates a boundary descriptor.
helpviewer_keywords: ["CreateBoundaryDescriptor","CreateBoundaryDescriptor function","CreateBoundaryDescriptorA","CreateBoundaryDescriptorW","base.createboundarydescriptor","winbase/CreateBoundaryDescriptor","winbase/CreateBoundaryDescriptorA","winbase/CreateBoundaryDescriptorW"]
old-location: base\createboundarydescriptor.htm
tech.root: backup
ms.assetid: c7789e90-8dfb-47ee-a0b2-906520982d84
ms.date: 08/03/2022
ms.keywords: CreateBoundaryDescriptor, CreateBoundaryDescriptor function, CreateBoundaryDescriptorA, CreateBoundaryDescriptorW, base.createboundarydescriptor, winbase/CreateBoundaryDescriptor, winbase/CreateBoundaryDescriptorA, winbase/CreateBoundaryDescriptorW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateBoundaryDescriptorA
 - winbase/CreateBoundaryDescriptorA
dev_langs:
 - c++
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
---

# CreateBoundaryDescriptorA function


## -description

Creates a boundary descriptor.

## -parameters

### -param Name [in]

The name of the boundary descriptor.

### -param Flags [in]

A combination of the following flags that are combined by using a bitwise **OR** operation.

| Flag                                                            | Description |
| --------------------------------------------------------------- | ----------- |
| **CREATE_BOUNDARY_DESCRIPTOR_ADD_APPCONTAINER_SID** (0x01)<br>**Note:** This value is not supported prior to Windows 8.     | Required for creating a boundary descriptor in an appcontainer process, regardless of producer or consumer.       |

## -returns

If the function succeeds, the return value is a handle to the boundary descriptor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A new boundary descriptor must have at least one security identifier (SID). To add a SID to a boundary descriptor, use the <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor">AddSIDToBoundaryDescriptor</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.

## -see-also

<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor">AddSIDToBoundaryDescriptor</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createprivatenamespacea">CreatePrivateNamespace</a>



<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-deleteboundarydescriptor">DeleteBoundaryDescriptor</a>



<a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>
