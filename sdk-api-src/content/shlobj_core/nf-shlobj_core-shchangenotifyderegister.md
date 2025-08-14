---
UID: NF:shlobj_core.SHChangeNotifyDeregister
title: SHChangeNotifyDeregister function (shlobj_core.h)
description: Unregisters the client's window process from receiving SHChangeNotify messages.
helpviewer_keywords: ["NTSHChangeNotifyDeregister","SHChangeNotifyDeregister","SHChangeNotifyDeregister function [Windows Shell]","_win32_SHChangeNotifyDeregister","shell.SHChangeNotifyDeregister","shlobj_core/NTSHChangeNotifyDeregister","shlobj_core/SHChangeNotifyDeregister"]
old-location: shell\SHChangeNotifyDeregister.htm
tech.root: shell
ms.assetid: fad021dc-8199-4384-b623-c98bc618799f
ms.date: 12/05/2018
ms.keywords: NTSHChangeNotifyDeregister, SHChangeNotifyDeregister, SHChangeNotifyDeregister function [Windows Shell], _win32_SHChangeNotifyDeregister, shell.SHChangeNotifyDeregister, shlobj_core/NTSHChangeNotifyDeregister, shlobj_core/SHChangeNotifyDeregister
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
 - SHChangeNotifyDeregister
 - shlobj_core/SHChangeNotifyDeregister
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
 - api-ms-win-shell-changenotify-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHChangeNotifyDeregister
 - NTSHChangeNotifyDeregister
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHChangeNotifyDeregister function


## -description

Unregisters the client's window process from receiving <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a> messages.

## -parameters

### -param ulID

Type: <b>ULONG</b>

A value of type <b>ULONG</b> that specifies the registration ID returned by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister">SHChangeNotifyRegister</a>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the specified client was found and removed; otherwise <b>FALSE</b>.

## -remarks

See the <a href="/previous-versions/windows/desktop/legacy/dd940348(v=vs.85)">Change Notify Watcher Sample</a> in the Windows Software Development Kit (SDK) for a full example that demonstrates the use of this function.

The <b>NTSHChangeNotifyDeregister</b> function, which is no longer available for use as of Windows Vista, was equivalent to <b>SHChangeNotifyDeregister</b>.
