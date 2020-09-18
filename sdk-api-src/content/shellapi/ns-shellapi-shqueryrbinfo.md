---
UID: NS:shellapi._SHQUERYRBINFO
title: SHQUERYRBINFO (shellapi.h)
description: Contains the size and item count information retrieved by the SHQueryRecycleBin function.
helpviewer_keywords: ["*LPSHQUERYRBINFO","LPSHQUERYRBINFO","LPSHQUERYRBINFO structure pointer [Windows Shell]","SHQUERYRBINFO","SHQUERYRBINFO structure [Windows Shell]","_win32_SHQUERYRBINFO","shell.SHQUERYRBINFO","shellapi/LPSHQUERYRBINFO","shellapi/SHQUERYRBINFO"]
old-location: shell\SHQUERYRBINFO.htm
tech.root: shell
ms.assetid: 7e9bc7e9-5712-45e7-a424-0afb62f26450
ms.date: 12/05/2018
ms.keywords: '*LPSHQUERYRBINFO, LPSHQUERYRBINFO, LPSHQUERYRBINFO structure pointer [Windows Shell], SHQUERYRBINFO, SHQUERYRBINFO structure [Windows Shell], _win32_SHQUERYRBINFO, shell.SHQUERYRBINFO, shellapi/LPSHQUERYRBINFO, shellapi/SHQUERYRBINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHQUERYRBINFO, *LPSHQUERYRBINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHQUERYRBINFO
 - shellapi/_SHQUERYRBINFO
 - LPSHQUERYRBINFO
 - shellapi/LPSHQUERYRBINFO
 - SHQUERYRBINFO
 - shellapi/SHQUERYRBINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - SHQUERYRBINFO
---

# SHQUERYRBINFO structure


## -description

Contains the size and item count information retrieved by the <a href="/windows/desktop/api/shellapi/nf-shellapi-shqueryrecyclebina">SHQueryRecycleBin</a> function.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. This member must be filled in prior to calling the function.

### -field i64Size

Type: <b>__int64</b>

The total size of all the objects in the specified Recycle Bin, in bytes.

### -field i64NumItems

Type: <b>__int64</b>

The total number of items in the specified Recycle Bin.