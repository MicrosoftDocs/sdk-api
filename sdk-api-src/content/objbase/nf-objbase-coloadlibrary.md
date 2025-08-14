---
UID: NF:objbase.CoLoadLibrary
title: CoLoadLibrary function (objbase.h)
description: Loads a specific DLL into the caller's process.
helpviewer_keywords: ["CoLoadLibrary","CoLoadLibrary function [COM]","_com_CoLoadLibrary","com.coloadlibrary","objbase/CoLoadLibrary"]
old-location: com\coloadlibrary.htm
tech.root: com
ms.assetid: be0d9e82-2438-488e-88c3-68dc7ac3e16f
ms.date: 12/05/2018
ms.keywords: CoLoadLibrary, CoLoadLibrary function [COM], _com_CoLoadLibrary, com.coloadlibrary, objbase/CoLoadLibrary
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoLoadLibrary
 - objbase/CoLoadLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - CoLoadLibrary
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CoLoadLibrary function


## -description

Loads a specific DLL into the caller's process.

<b>CoLoadLibrary</b> is equivalent to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>. <b>CoLoadLibrary</b> does not affect the lifetime of the library.

## -parameters

### -param lpszLibName [in]

The name of the library to be loaded.

### -param bAutoFree [in]

This parameter is maintained for compatibility with 16-bit applications, but is ignored.

## -returns

If the function succeeds, the return value is a handle to the loaded library; otherwise, it is <b>NULL</b>.

## -remarks

The <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a> function does not call <b>CoLoadLibrary</b>. <b>CoLoadLibrary</b> loads a DLL specified by the <i>lpszLibName</i> parameter into the process that called <b>CoGetClassObject</b>. Containers should not call <b>CoLoadLibrary</b> directly.

Internally, a reference count is kept on the loaded DLL by using <b>CoLoadLibrary</b> to increment the count and the <a href="/windows/desktop/api/objbase/nf-objbase-cofreelibrary">CoFreeLibrary</a> function to decrement it.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-cofreealllibraries">CoFreeAllLibraries</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cofreelibrary">CoFreeLibrary</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibrariesex">CoFreeUnusedLibrariesEx</a>
