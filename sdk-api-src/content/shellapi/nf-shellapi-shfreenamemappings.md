---
UID: NF:shellapi.SHFreeNameMappings
title: SHFreeNameMappings function (shellapi.h)
description: Frees a file name mapping object that was retrieved by the SHFileOperation function.
helpviewer_keywords: ["SHFreeNameMappings","SHFreeNameMappings function [Windows Shell]","_win32_SHFreeNameMappings","shell.SHFreeNameMappings","shellapi/SHFreeNameMappings"]
old-location: shell\SHFreeNameMappings.htm
tech.root: shell
ms.assetid: 4552b2e0-9257-48f8-84cc-003217f1696f
ms.date: 12/05/2018
ms.keywords: SHFreeNameMappings, SHFreeNameMappings function [Windows Shell], _win32_SHFreeNameMappings, shell.SHFreeNameMappings, shellapi/SHFreeNameMappings
req.header: shellapi.h
req.include-header: 
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFreeNameMappings
 - shellapi/SHFreeNameMappings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHFreeNameMappings
---

# SHFreeNameMappings function


## -description

Frees a file name mapping object that was retrieved by the <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.

## -parameters

### -param hNameMappings [in, optional]

Type: <b>HANDLE</b>

A handle to the file name mapping object to be freed.