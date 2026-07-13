---
UID: NF:combaseapi.CoFreeUnusedLibraries
title: CoFreeUnusedLibraries function (combaseapi.h)
description: Unloads any DLLs that are no longer in use, probably because the DLL no longer has any instantiated COM objects outstanding.
helpviewer_keywords: ["CoFreeUnusedLibraries","CoFreeUnusedLibraries function [COM]","_com_CoFreeUnusedLibraries","com.cofreeunusedlibraries","combaseapi/CoFreeUnusedLibraries"]
old-location: com\cofreeunusedlibraries.htm
tech.root: com
ms.assetid: 188e9a3b-39cc-454e-af65-4ac797e275d4
ms.date: 12/05/2018
ms.keywords: CoFreeUnusedLibraries, CoFreeUnusedLibraries function [COM], _com_CoFreeUnusedLibraries, com.cofreeunusedlibraries, combaseapi/CoFreeUnusedLibraries
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CoFreeUnusedLibraries
 - combaseapi/CoFreeUnusedLibraries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoFreeUnusedLibraries
---

# CoFreeUnusedLibraries function


## -description

Unloads any DLLs that are no longer in use, probably because the DLL no longer has any instantiated COM objects outstanding.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>



## -remarks

Applications can call <b>CoFreeUnusedLibraries</b> periodically to free resources. It is most efficient to call it either at the top of a message loop or in some idle-time task. <b>CoFreeUnusedLibraries</b> internally calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a> for DLLs that implement and export that function.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-cofreealllibraries">CoFreeAllLibraries</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cofreelibrary">CoFreeLibrary</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibrariesex">CoFreeUnusedLibrariesEx</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a>
