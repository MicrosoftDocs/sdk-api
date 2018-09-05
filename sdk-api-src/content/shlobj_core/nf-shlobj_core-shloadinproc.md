---
UID: NF:shlobj_core.SHLoadInProc
title: SHLoadInProc function
author: windows-sdk-content
description: Creates an instance of the specified object class from within the context of the Shell's process. Windows Vista and later:\_This function has been disabled and returns E_NOTIMPL.
old-location: shell\SHLoadInProc.htm
old-project: shell
ms.assetid: 307b99d9-2d0a-47c5-8a10-dfdc0a408942
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHLoadInProc, SHLoadInProc function [Windows Shell], _win32_SHLoadInProc, shell.SHLoadInProc, shlobj_core/SHLoadInProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHLoadInProc
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHLoadInProc function


## -description


Creates an instance of the specified object class from within the context of the Shell's process.
        
            

<b>Windows Vista</b> and later: This function has been disabled and returns E_NOTIMPL.


## -parameters




### -param rclsid [in]

Type: <b>REFCLSID</b>

The CLSID of the object class to be created.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In Windows Vista and later versions, always returns E_NOTIMPL.




## -remarks



<div class="alert"><b>Note</b>  This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It is not available in later versions of Windows, including Windows Vista.</div>
<div> </div>
This function creates the requested object instance by calling the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function and immediately releasing the returned object. The associated DLL is unloaded according to standard Component Object Model (COM) rules when it returns S_OK from its <a href="https://msdn.microsoft.com/a47df9eb-97cb-4875-a121-1dabe7bc9db6">DllCanUnloadNow</a> function.



