---
UID: NF:winbase.CreatePrivateNamespaceA
title: CreatePrivateNamespaceA function
author: windows-sdk-content
description: Creates a private namespace.
old-location: base\createprivatenamespace.htm
old-project: Sync
ms.assetid: bb6331b0-88cb-4695-b159-6e8750440a69
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreatePrivateNamespace, CreatePrivateNamespace function, CreatePrivateNamespaceA, CreatePrivateNamespaceW, base.createprivatenamespace, winbase/CreatePrivateNamespace, winbase/CreatePrivateNamespaceA, winbase/CreatePrivateNamespaceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreatePrivateNamespaceW (Unicode) and CreatePrivateNamespaceA (ANSI)
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
 - CreatePrivateNamespace
 - CreatePrivateNamespaceA
 - CreatePrivateNamespaceW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreatePrivateNamespaceA function


## -description


Creates a private namespace.


## -parameters




### -param lpPrivateNamespaceAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies the security attributes of the namespace object.


### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The caller must be within this boundary. The <a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a> function creates a boundary descriptor.


### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as <i>prefix</i>\<i>objectname</i>.

The system supports multiple private namespaces with the same name, as long as they define different boundaries.


## -returns



If the function succeeds, it returns a handle to the new namespace. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
     




## -remarks



Other applications can access the namespace using the <a href="https://msdn.microsoft.com/268b4932-2553-4883-8a26-002997fbc59e">OpenPrivateNamespace</a> function.

The application that created the namespace can use the <a href="https://msdn.microsoft.com/b9b74cf2-bf13-4ceb-9242-bc6a884ac6f1">ClosePrivateNamespace</a> function to close the handle to the namespace. The handle is also closed when the creating process terminates. After the namespace handle is closed, subsequent calls to <a href="https://msdn.microsoft.com/268b4932-2553-4883-8a26-002997fbc59e">OpenPrivateNamespace</a> fail, but all operations on objects in the namespace succeed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/b9b74cf2-bf13-4ceb-9242-bc6a884ac6f1">ClosePrivateNamespace</a>



<a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>



<a href="https://msdn.microsoft.com/268b4932-2553-4883-8a26-002997fbc59e">OpenPrivateNamespace</a>
 

 

