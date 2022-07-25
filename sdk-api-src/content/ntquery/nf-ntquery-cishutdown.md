---
UID: NF:ntquery.CIShutdown
title: CIShutdown function (ntquery.h)
description: Shuts down the content indexer and closes all open catalogs.
helpviewer_keywords: ["CIShutdown","CIShutdown function [Windows Shell]","_shell_CIShutdown","ntquery/CIShutdown","shell.CIShutdown"]
old-location: shell\CIShutdown.htm
tech.root: shell
ms.assetid: 16c932a6-8def-4ff9-b531-03ebd011086a
ms.date: 12/05/2018
ms.keywords: CIShutdown, CIShutdown function [Windows Shell], _shell_CIShutdown, ntquery/CIShutdown, shell.CIShutdown
f1_keywords:
- ntquery/CIShutdown
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Query.dll (version 5.1 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Query.dll
api_name:
- CIShutdown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIShutdown function


## -description


Shuts down the content indexer and closes all open catalogs.
        
            
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.</div><div> </div>








## -returns



This function does not return a value.




## -remarks



This function does not have an associated header or library file. To use this function, call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> with the DLL name (Query.dll) to obtain a module handle, and then call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> with that module handle and an architecture-specific function name to get the address of this function. Specify the function name as "<b>?CIShutdown@@YGXXZ</b>" for x86 architecture, or as "<b>?CIShutdown@@YAXXZ</b>" for x64 architecture.
