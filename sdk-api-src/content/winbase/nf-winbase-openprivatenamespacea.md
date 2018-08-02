---
UID: NF:winbase.OpenPrivateNamespaceA
title: OpenPrivateNamespaceA function
author: windows-sdk-content
description: Opens a private namespace.
old-location: base\openprivatenamespace.htm
old-project: Sync
ms.assetid: 268b4932-2553-4883-8a26-002997fbc59e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: OpenPrivateNamespace, OpenPrivateNamespace function, OpenPrivateNamespaceA, OpenPrivateNamespaceW, base.openprivatenamespace, winbase/OpenPrivateNamespace, winbase/OpenPrivateNamespaceA, winbase/OpenPrivateNamespaceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OpenPrivateNamespaceA function


## -description


Opens a private namespace.


## -parameters




### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The <a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a> function creates a boundary descriptor.


### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as <i>prefix</i>\<i>objectname</i>.


## -returns



The function returns the handle to the existing namespace.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/b9b74cf2-bf13-4ceb-9242-bc6a884ac6f1">ClosePrivateNamespace</a>



<a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a>



<a href="https://msdn.microsoft.com/bb6331b0-88cb-4695-b159-6e8750440a69">CreatePrivateNamespace</a>



<a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>
 

 

