---
UID: NF:shlobj.PerUserInit
title: PerUserInit function
author: windows-sdk-content
description: Creates My Documents and other special folders, initializes them as needed, and creates the Send To shortcut menu item for My Documents.
old-location: shell\PerUserInit.htm
old-project: shell
ms.assetid: 08ce75e9-3316-4967-925e-25b15fc97aa0
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: PerUserInit, PerUserInit function [Windows Shell], _win32_PerUserInit, shell.PerUserInit, shlobj/PerUserInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj.h
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mydocs.dll
api_name:
 - PerUserInit
product: Windows
targetos: Windows
req.lib: 
req.dll: Mydocs.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# PerUserInit function


## -description


<p class="CCE_Message">[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates <a href="https://msdn.microsoft.com/d9ffda6f-adc0-44a3-b410-e23bf5f4f165">My Documents</a> and other special folders, initializes them as needed, and creates the <b>Send To</b> shortcut menu item for My Documents. 
        


## -parameters






## -returns



This function does not return a value.




## -remarks



Applications do not need to call this function because the operating system already does so.

This function does not have an associated header or library file so it must be called by ordinal value. Call <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> with the DLL name Mydocs.dll to obtain a module handle. Then call <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> with that module handle and the ordinal number 7 to use this function.



