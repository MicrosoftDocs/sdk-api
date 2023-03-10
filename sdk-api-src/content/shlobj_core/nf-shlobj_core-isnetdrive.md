---
UID: NF:shlobj_core.IsNetDrive
title: IsNetDrive function (shlobj_core.h)
description: Tests whether a drive is a network drive.
helpviewer_keywords: ["IsNetDrive","IsNetDrive function [Windows Shell]","_win32_IsNetDrive","shell.IsNetDrive","shlobj_core/IsNetDrive"]
old-location: shell\IsNetDrive.htm
tech.root: shell
ms.assetid: 44e02665-648a-4cf0-9dc0-038e54d08a49
ms.date: 12/05/2018
ms.keywords: IsNetDrive, IsNetDrive function [Windows Shell], _win32_IsNetDrive, shell.IsNetDrive, shlobj_core/IsNetDrive
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsNetDrive
 - shlobj_core/IsNetDrive
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
 - IsNetDrive
---

# IsNetDrive function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a> or <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a> instead.]

Tests whether a drive is a network drive.

## -parameters

### -param iDrive [in]

Type: <b>int</b>

An integer that indicates which drive letter you want to test. Set it to 0 for  A:, 1 for B:, and so on.

## -returns

Type: <b>int</b>

This function returns one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The specified drive is not a network drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The specified drive is a network drive that is properly connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The specified drive is a network drive that is disconnected or in an error state.

</td>
</tr>
</table>