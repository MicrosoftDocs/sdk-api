---
UID: NF:winbase.CreatePrivateNamespaceA
title: CreatePrivateNamespaceA function (winbase.h)
description: Creates a private namespace.
old-location: base\createprivatenamespace.htm
tech.root: Sync
ms.assetid: bb6331b0-88cb-4695-b159-6e8750440a69
ms.date: 12/05/2018
ms.keywords: CreatePrivateNamespace, CreatePrivateNamespace function, CreatePrivateNamespaceA, CreatePrivateNamespaceW, base.createprivatenamespace, winbase/CreatePrivateNamespace, winbase/CreatePrivateNamespaceA, winbase/CreatePrivateNamespaceW
f1_keywords:
- winbase/CreatePrivateNamespace
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
req.unicode-ansi: CreatePrivateNamespaceW (Unicode) and CreatePrivateNamespaceA (ANSI)
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
- CreatePrivateNamespace
- CreatePrivateNamespaceA
- CreatePrivateNamespaceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreatePrivateNamespaceA function


## -description


Creates a private namespace.


## -parameters




### -param lpPrivateNamespaceAttributes [in, optional]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> structure that specifies the security attributes of the namespace object.


### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The caller must be within this boundary. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a> function creates a boundary descriptor.


### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as _prefix_\\_objectname_.

The system supports multiple private namespaces with the same name, as long as they define different boundaries.


## -returns



If the function succeeds, it returns a handle to the new namespace. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
     




## -remarks



Other applications can access the namespace using the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openprivatenamespacea">OpenPrivateNamespace</a> function.

The application that created the namespace can use the <a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a> function to close the handle to the namespace. The handle is also closed when the creating process terminates. After the namespace handle is closed, subsequent calls to <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openprivatenamespacea">OpenPrivateNamespace</a> fail, but all operations on objects in the namespace succeed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openprivatenamespacea">OpenPrivateNamespace</a>
 

 


