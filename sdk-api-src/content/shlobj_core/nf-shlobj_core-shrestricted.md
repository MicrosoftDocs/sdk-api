---
UID: NF:shlobj_core.SHRestricted
title: SHRestricted function (shlobj_core.h)
description: SHRestricted may be altered or unavailable.
helpviewer_keywords: ["SHRestricted","SHRestricted function [Windows Shell]","_win32_SHRestricted","shell.SHRestricted","shlobj_core/SHRestricted"]
old-location: shell\SHRestricted.htm
tech.root: shell
ms.assetid: 94adf343-3879-455a-9770-70460cf383ca
ms.date: 12/05/2018
ms.keywords: SHRestricted, SHRestricted function [Windows Shell], _win32_SHRestricted, shell.SHRestricted, shlobj_core/SHRestricted
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRestricted
 - shlobj_core/SHRestricted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHRestricted
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHRestricted function


## -description

<p class="CCE_Message">[<b>SHRestricted</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a specified administrator policy is in effect. In many cases, applications need to modify certain behaviors to comply with the policies enacted by system administrators.

## -parameters

### -param rest

Type: <b><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions">RESTRICTIONS</a></b>

Specifies one of the flags described in the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions">RESTRICTIONS</a> enumerated type.

## -returns

Type: <b>DWORD</b>

Returns nonzero if the specified restriction is in effect, or zero otherwise.
