---
UID: NF:shlwapi.SHRegDuplicateHKey
title: SHRegDuplicateHKey function (shlwapi.h)
description: Duplicates a registry key's HKEY handle.
helpviewer_keywords: ["SHRegDuplicateHKey","SHRegDuplicateHKey function [Windows Shell]","_win32_SHRegDuplicateHKey","shell.SHRegDuplicateHKey","shlwapi/SHRegDuplicateHKey"]
old-location: shell\SHRegDuplicateHKey.htm
tech.root: shell
ms.assetid: 73182aa9-0c4d-4723-ba3c-8bab6b51181b
ms.date: 12/05/2018
ms.keywords: SHRegDuplicateHKey, SHRegDuplicateHKey function [Windows Shell], _win32_SHRegDuplicateHKey, shell.SHRegDuplicateHKey, shlwapi/SHRegDuplicateHKey
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegDuplicateHKey
 - shlwapi/SHRegDuplicateHKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-Registry-l1-1-0.dll
 - API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
 - SHRegDuplicateHKey
---

# SHRegDuplicateHKey function


## -description

Duplicates a registry key's HKEY handle.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

The HKEY handle to be duplicated.

## -returns

Type: <b>HKEY</b>

Returns a duplicate of the handle specified in <i>hkey</i>.

