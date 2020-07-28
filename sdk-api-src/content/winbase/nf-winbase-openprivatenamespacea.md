---
UID: NF:winbase.OpenPrivateNamespaceA
title: OpenPrivateNamespaceA function (winbase.h)
description: Opens a private namespace.
helpviewer_keywords: ["OpenPrivateNamespace","OpenPrivateNamespace function","OpenPrivateNamespaceA","OpenPrivateNamespaceW","base.openprivatenamespace","winbase/OpenPrivateNamespace","winbase/OpenPrivateNamespaceA","winbase/OpenPrivateNamespaceW"]
old-location: base\openprivatenamespace.htm
tech.root: backup
ms.assetid: 268b4932-2553-4883-8a26-002997fbc59e
ms.date: 12/05/2018
ms.keywords: OpenPrivateNamespace, OpenPrivateNamespace function, OpenPrivateNamespaceA, OpenPrivateNamespaceW, base.openprivatenamespace, winbase/OpenPrivateNamespace, winbase/OpenPrivateNamespaceA, winbase/OpenPrivateNamespaceW
f1_keywords:
- winbase/OpenPrivateNamespace
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
req.unicode-ansi: OpenPrivateNamespaceW (Unicode) and OpenPrivateNamespaceA (ANSI)
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
- OpenPrivateNamespace
- OpenPrivateNamespaceA
- OpenPrivateNamespaceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenPrivateNamespaceA function


## -description


Opens a private namespace.


## -parameters




### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a> function creates a boundary descriptor.


### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as _prefix_\\_objectname_.


## -returns



The function returns the handle to the existing namespace.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprivatenamespacea">CreatePrivateNamespace</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>
 
