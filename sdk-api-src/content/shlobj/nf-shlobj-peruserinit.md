---
UID: NF:shlobj.PerUserInit
title: PerUserInit function (shlobj.h)
description: Creates My Documents and other special folders, initializes them as needed, and creates the Send To shortcut menu item for My Documents.
helpviewer_keywords: ["PerUserInit","PerUserInit function [Windows Shell]","_win32_PerUserInit","shell.PerUserInit","shlobj/PerUserInit"]
old-location: shell\PerUserInit.htm
tech.root: shell
ms.assetid: 08ce75e9-3316-4967-925e-25b15fc97aa0
ms.date: 12/05/2018
ms.keywords: PerUserInit, PerUserInit function [Windows Shell], _win32_PerUserInit, shell.PerUserInit, shlobj/PerUserInit
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
req.lib: 
req.dll: Mydocs.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerUserInit
 - shlobj/PerUserInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mydocs.dll
api_name:
 - PerUserInit
---

# PerUserInit function


## -description

<p class="CCE_Message">[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates <a href="/windows/desktop/shell/manage">My Documents</a> and other special folders, initializes them as needed, and creates the <b>Send To</b> shortcut menu item for My Documents.



## -remarks

Applications do not need to call this function because the operating system already does so.

This function does not have an associated header or library file so it must be called by ordinal value. Call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> with the DLL name Mydocs.dll to obtain a module handle. Then call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> with that module handle and the ordinal number 7 to use this function.
