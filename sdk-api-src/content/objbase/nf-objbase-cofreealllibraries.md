---
UID: NF:objbase.CoFreeAllLibraries
title: CoFreeAllLibraries function (objbase.h)
author: windows-sdk-content
description: Frees all the DLLs that have been loaded with the CoLoadLibrary function (called internally by CoGetClassObject), regardless of whether they are currently in use.
old-location: com\cofreealllibraries.htm
tech.root: com
ms.assetid: 20616c05-21c6-4895-a1b5-4bae1aa417c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoFreeAllLibraries, CoFreeAllLibraries function [COM], _com_CoFreeAllLibraries, com.cofreealllibraries, objbase/CoFreeAllLibraries
ms.topic: function
f1_keywords: 
 - "objbase/CoFreeAllLibraries"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoFreeAllLibraries
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoFreeAllLibraries function


## -description


Frees all the DLLs that have been loaded with the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a> function (called internally by <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>), regardless of whether they are currently in use.


## -parameters






## -returns



This function does not return a value.




## -remarks



To unload libraries, <b>CoFreeAllLibraries</b> uses a list of loaded DLLs for each process that the COM library maintains. The <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a> functions call <b>CoFreeAllLibraries</b> internally, so applications usually have no need to call this function directly.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cofreelibrary">CoFreeLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries">CoFreeUnusedLibraries</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibrariesex">CoFreeUnusedLibrariesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coloadlibrary">CoLoadLibrary</a>
 

 

