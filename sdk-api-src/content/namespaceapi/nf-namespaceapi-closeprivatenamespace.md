---
UID: NF:namespaceapi.ClosePrivateNamespace
title: ClosePrivateNamespace function (namespaceapi.h)
description: Closes an open namespace handle.helpviewer_keywords: ["ClosePrivateNamespace","ClosePrivateNamespace function","base.closeprivatenamespace","namespaceapi/ClosePrivateNamespace","winbase/ClosePrivateNamespace"]
old-location: base\closeprivatenamespace.htm
tech.root: Sync
ms.assetid: b9b74cf2-bf13-4ceb-9242-bc6a884ac6f1
ms.date: 12/05/2018
ms.keywords: ClosePrivateNamespace, ClosePrivateNamespace function, base.closeprivatenamespace, namespaceapi/ClosePrivateNamespace, winbase/ClosePrivateNamespace
f1_keywords:
- namespaceapi/ClosePrivateNamespace
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
- ClosePrivateNamespace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClosePrivateNamespace function


## -description


Closes an open namespace handle.


## -parameters




### -param Handle [in]

The namespace handle. This handle is created by <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprivatenamespacea">CreatePrivateNamespace</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openprivatenamespacea">OpenPrivateNamespace</a>.


### -param Flags [in]

If this parameter is <b>PRIVATE_NAMESPACE_FLAG_DESTROY</b> (0x00000001), the namespace is destroyed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createprivatenamespacea">CreatePrivateNamespace</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openprivatenamespacea">OpenPrivateNamespace</a>
 

 

