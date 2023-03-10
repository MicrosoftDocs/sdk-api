---
UID: NC:ntsecpkg.LSA_CREATE_THREAD
title: LSA_CREATE_THREAD (ntsecpkg.h)
description: A wrapper for the Windows CreateThread function that should be used by the Local Security Authority (LSA).
helpviewer_keywords: ["CreateThread","CreateThread callback function [Security]","LSA_CREATE_THREAD","LSA_CREATE_THREAD callback","_ssp_createthread","ntsecpkg/CreateThread","security.createthread"]
old-location: security\createthread.htm
tech.root: security
ms.assetid: dc02abb9-ab05-4a7f-a125-15530619633b
ms.date: 12/05/2018
ms.keywords: CreateThread, CreateThread callback function [Security], LSA_CREATE_THREAD, LSA_CREATE_THREAD callback, _ssp_createthread, ntsecpkg/CreateThread, security.createthread
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_CREATE_THREAD
 - ntsecpkg/LSA_CREATE_THREAD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - CreateThread
---

# LSA_CREATE_THREAD callback function


## -description

The <b>CreateThread</b> function is a wrapper for the Windows 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a> function that should be used by the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA). It creates a thread that the LSA can track, attaches debugging information to threads it starts, and provides special exception handling to protect the LSA process.

## -parameters

### -param SecurityAttributes [in]

Pointer to a <b>SEC_ATTRS</b> structure that determines whether the returned handle can be inherited by child processes.

### -param StackSize [in]

Specifies the initial commit size of the stack, in bytes.

### -param StartFunction [in]

Pointer to the application-defined function of type <b>SEC_THREAD_START</b> to be executed by the thread.

### -param ThreadParameter [in]

Pointer to a single parameter value passed to the thread.

### -param CreationFlags [in]

Specifies flags that control the creation of the thread.

### -param ThreadId [out]

Pointer to a variable that receives the thread identifier.

## -returns

If the function succeeds, the return value is a handle to the new thread. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A pointer to the <b>CreateThread</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

For more information, see the Windows 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a> function.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>