---
UID: NF:namespaceapi.OpenPrivateNamespaceW
tech.root: Sync 
title: OpenPrivateNamespaceW
ms.date: 08/05/2022
targetos: Windows
description: The OpenPrivateNamespaceW (Unicode) function (namespaceapi.h) opens a private namespace. 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll:  Kernel32.dll 
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
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - OpenPrivateNamespaceW
f1_keywords:
 - OpenPrivateNamespaceW
 - namespaceapi/OpenPrivateNamespaceW
dev_langs:
 - c++
---

# OpenPrivateNamespaceW function

## -description

Opens a private namespace.

## -parameters

### -param lpBoundaryDescriptor [in]

A descriptor that defines how the namespace is to be isolated. The <a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-createboundarydescriptorw">CreateBoundaryDescriptor</a> function creates a boundary descriptor.

### -param lpAliasPrefix [in]

The prefix for the namespace. To create an object in this namespace, specify the object name as <i>prefix</i>&#92;<i>objectname</i>.

## -returns

The function returns the handle to the existing namespace.

## -remarks

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.

## -see-also

<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-closeprivatenamespace">ClosePrivateNamespace</a>  
<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-createboundarydescriptorw">CreateBoundaryDescriptor</a>  
<a href="/windows/desktop/api/namespaceapi/nf-namespaceapi-createprivatenamespacew">CreatePrivateNamespace</a>  
<a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>  
