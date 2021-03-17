---
UID: NF:shlobj_core.SHValidateUNC
title: SHValidateUNC function (shlobj_core.h)
description: SHValidateUNC may be altered or unavailable.
helpviewer_keywords: ["SHValidateUNC","SHValidateUNC function [Windows Shell]","VALIDATEUNC_CONNECT","VALIDATEUNC_NOUI","VALIDATEUNC_PERSIST","VALIDATEUNC_PRINT","VALIDATEUNC_VALID","_win32_SHValidateUNC","shell.SHValidateUNC","shlobj_core/SHValidateUNC"]
old-location: shell\SHValidateUNC.htm
tech.root: shell
ms.assetid: 42394650-5571-4165-84f1-19a26fb4a1b8
ms.date: 12/05/2018
ms.keywords: SHValidateUNC, SHValidateUNC function [Windows Shell], VALIDATEUNC_CONNECT, VALIDATEUNC_NOUI, VALIDATEUNC_PERSIST, VALIDATEUNC_PRINT, VALIDATEUNC_VALID, _win32_SHValidateUNC, shell.SHValidateUNC, shlobj_core/SHValidateUNC
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHValidateUNC
 - shlobj_core/SHValidateUNC
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
 - SHValidateUNC
---

# SHValidateUNC function


## -description

<p class="CCE_Message">[<b>SHValidateUNC</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Validates a Universal Naming Convention (UNC) path by calling <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a">WNetAddConnection3</a>. The function makes it possible for the user to type a remote network access (RNA) UNC application or document name from the <b>Run</b> dialog box on the <b>Start</b> menu.

## -parameters

### -param hwndOwner [in, optional]

Type: <b>HWND</b>

Handle of the parent window, used to display UI. If this is not needed, this value can be set to <b>NULL</b>.

### -param pszFile [in, out]

Type: <b>PWSTR</b>

A pointer to a null-terminated Unicode string that specifies the UNC path to validate. Note: This string must not be a constant string.

### -param fConnect

Type: <b>UINT</b>

One or more of the following values.



#### VALIDATEUNC_CONNECT (0x0001)

Connect a drive letter. When this flag is set, the value in <i>pszFile</i> is changed to the local drive to which the UNC is mapped on the local machine.



#### VALIDATEUNC_NOUI (0x0002)

On either failure or success, display no UI.



#### VALIDATEUNC_PRINT (0x0004)

Validate as a print share rather than disk share.



#### VALIDATEUNC_PERSIST (0x0008)

<b>Windows Vista and later</b>. The connection should be made persistent.



#### VALIDATEUNC_VALID

Mask value used to verify that the flags passed to <b>SHValidateUNC</b> are valid.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the UNC path exists; <b>FALSE</b> if the UNC path does not exist or if some other failure occurred.