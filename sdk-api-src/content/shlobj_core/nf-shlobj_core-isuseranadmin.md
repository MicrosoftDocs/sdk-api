---
UID: NF:shlobj_core.IsUserAnAdmin
title: IsUserAnAdmin function (shlobj_core.h)
description: IsUserAnAdmin may be altered or unavailable.
helpviewer_keywords: ["IsUserAnAdmin","IsUserAnAdmin function [Windows Shell]","_win32_IsUserAnAdmin","shell.IsUserAnAdmin","shlobj_core/IsUserAnAdmin"]
old-location: shell\IsUserAnAdmin.htm
tech.root: shell
ms.assetid: fe698d32-32f6-4b2b-ad0c-5d9ec815177f
ms.date: 12/05/2018
ms.keywords: IsUserAnAdmin, IsUserAnAdmin function [Windows Shell], _win32_IsUserAnAdmin, shell.IsUserAnAdmin, shlobj_core/IsUserAnAdmin
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
 - IsUserAnAdmin
 - shlobj_core/IsUserAnAdmin
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
 - IsUserAnAdmin
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# IsUserAnAdmin function


## -description

<p class="CCE_Message">[<b>IsUserAnAdmin</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Tests whether the current user is a member of the Administrator's group.



## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the user is a member of the Administrator's group; otherwise, <b>FALSE</b>.

## -remarks

This function is a wrapper for <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a>. It is recommended to call that function directly to determine Administrator group status rather than calling  <b>IsUserAnAdmin</b>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a>
