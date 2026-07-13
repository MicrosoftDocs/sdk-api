---
UID: NF:shlobj_core.SHGetSetSettings
title: SHGetSetSettings function (shlobj_core.h)
description: SHGetSetSettings may be altered or unavailable.
helpviewer_keywords: ["SHGetSetSettings","SHGetSetSettings function [Windows Shell]","_win32_SHGetSetSettings","shell.SHGetSetSettings","shlobj_core/SHGetSetSettings"]
old-location: shell\SHGetSetSettings.htm
tech.root: shell
ms.assetid: d7c2646c-03e0-4d7a-9503-bdf487d43723
ms.date: 12/05/2018
ms.keywords: SHGetSetSettings, SHGetSetSettings function [Windows Shell], _win32_SHGetSetSettings, shell.SHGetSetSettings, shlobj_core/SHGetSetSettings
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
 - SHGetSetSettings
 - shlobj_core/SHGetSetSettings
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
api_name:
 - SHGetSetSettings
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHGetSetSettings function


## -description

<p class="CCE_Message">[<b>SHGetSetSettings</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets or retrieves Shell state settings.

## -parameters

### -param lpss [in, out]

Type: <b>LPSHELLSTATE</b>

A pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea">SHELLSTATE</a> structure that provides or receives the Shell state settings.

### -param dwMask [in]

Type: <b>DWORD</b>

One or more of the <a href="/windows/desktop/shell/ssf-constants">SSF</a> flags that indicate which settings should be set or retrieved.

### -param bSet [in]

Type: <b>BOOL</b>

<b>TRUE</b> to indicate that the contents of <i>lpss</i> should be used to set the Shell settings, <b>FALSE</b> to indicate that the Shell settings should be retrieved to <i>lpss</i>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings">SHGetSettings</a>
