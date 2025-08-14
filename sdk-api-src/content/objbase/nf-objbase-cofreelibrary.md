---
UID: NF:objbase.CoFreeLibrary
title: CoFreeLibrary function (objbase.h)
description: Frees a library that, when loaded, was specified to be freed explicitly.
helpviewer_keywords: ["CoFreeLibrary","CoFreeLibrary function [COM]","_com_CoFreeLibrary","com.cofreelibrary","objbase/CoFreeLibrary"]
old-location: com\cofreelibrary.htm
tech.root: com
ms.assetid: 3959e7d9-6220-474e-8f85-76f7f935727f
ms.date: 12/05/2018
ms.keywords: CoFreeLibrary, CoFreeLibrary function [COM], _com_CoFreeLibrary, com.cofreelibrary, objbase/CoFreeLibrary
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
 - CoFreeLibrary
 - objbase/CoFreeLibrary
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
 - CoFreeLibrary
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CoFreeLibrary function


## -description

Frees a library that, when loaded, was specified to be freed explicitly.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters

### -param hInst [in]

A handle to the library module to be freed, as returned by the <a href="/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a> function.

## -remarks

The <b>CoFreeLibrary</b> function should be called to free a library that is to be freed explicitly. This is established when the library is loaded with the <i>bAutoFree</i> parameter of <a href="/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a> set to <b>FALSE</b>. It is illegal to free a library explicitly when the corresponding <b>CoLoadLibrary</b> call specifies that it be freed automatically (the <i>bAutoFree</i> parameter is set to <b>TRUE</b>).

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-cofreealllibraries">CoFreeAllLibraries</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibrariesex">CoFreeUnusedLibrariesEx</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a>
