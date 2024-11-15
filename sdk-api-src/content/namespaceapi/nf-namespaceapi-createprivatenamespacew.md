---
UID: NF:namespaceapi.CreatePrivateNamespaceW
tech.root: Sync 
title: CreatePrivateNamespaceW
ms.date: 08/05/2022
targetos: Windows
description: The CreatePrivateNamespaceW (Unicode) function (namespaceapi.h) creates a private namespace. 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll 
req.header: namespaceapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
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
 - CreatePrivateNamespaceW
f1_keywords:
 - CreatePrivateNamespaceW
 - namespaceapi/CreatePrivateNamespaceW
dev_langs:
 - c++
---

# CreatePrivateNamespaceW function

## -description

Creates a private namespace.

## -parameters

### -param lpPrivateNamespaceAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies the security attributes of the namespace object.

### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The caller must be within this boundary. The <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-createboundarydescriptorw">CreateBoundaryDescriptor</a> function creates a boundary descriptor.

### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as <i>prefix</i>&#92;<i>objectname</i>.

The system supports multiple private namespaces with the same name, as long as they define different boundaries.

## -returns

If the function succeeds, it returns a handle to the new namespace. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Other applications can access the namespace using the <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-openprivatenamespacew">OpenPrivateNamespace</a> function.

The application that created the namespace can use the <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a> function to close the handle to the namespace. The handle is also closed when the creating process terminates. After the namespace handle is closed, subsequent calls to <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-openprivatenamespacew">OpenPrivateNamespace</a> fail, but all operations on objects in the namespace succeed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.

## -see-also

<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a>  
<a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>  
<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-openprivatenamespacew">OpenPrivateNamespace</a>  
