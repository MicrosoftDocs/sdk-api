---
UID: NF:shlobj_core.SHStartNetConnectionDialogW
title: SHStartNetConnectionDialogW function (shlobj_core.h)
description: SHStartNetConnectionDialog may be altered or unavailable. (Unicode)
helpviewer_keywords: ["RESOURCETYPE_ANY", "RESOURCETYPE_DISK", "RESOURCETYPE_PRINT", "SHStartNetConnectionDialog", "SHStartNetConnectionDialog function [Windows Shell]", "SHStartNetConnectionDialogW", "_win32_SHStartNetConnectionDialog", "shell.SHStartNetConnectionDialog", "shlobj_core/SHStartNetConnectionDialog", "shlobj_core/SHStartNetConnectionDialogW"]
old-location: shell\SHStartNetConnectionDialog.htm
tech.root: shell
ms.assetid: 9de9d5f4-a89f-42d2-b24e-b037694f6e92
ms.date: 12/05/2018
ms.keywords: RESOURCETYPE_ANY, RESOURCETYPE_DISK, RESOURCETYPE_PRINT, SHStartNetConnectionDialog, SHStartNetConnectionDialog function [Windows Shell], SHStartNetConnectionDialogA, SHStartNetConnectionDialogW, _win32_SHStartNetConnectionDialog, shell.SHStartNetConnectionDialog, shlobj_core/SHStartNetConnectionDialog, shlobj_core/SHStartNetConnectionDialogA, shlobj_core/SHStartNetConnectionDialogW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHStartNetConnectionDialogW (Unicode) and SHStartNetConnectionDialogA (ANSI)
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
 - SHStartNetConnectionDialogW
 - shlobj_core/SHStartNetConnectionDialogW
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
 - SHStartNetConnectionDialog
 - SHStartNetConnectionDialogA
 - SHStartNetConnectionDialogW
---

# SHStartNetConnectionDialogW function


## -description

<p class="CCE_Message">[<b>SHStartNetConnectionDialog</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a general browsing dialog box for a network resource connection.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.

### -param pszRemoteName [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated character string that specifies the remote network name. This value can be set to <b>NULL</b>.

### -param dwType

Type: <b>DWORD</b>

A bitfield that contains a set of flags that identify the type of resource that the dialog box is set to find. This value can contain one of the following values, defined in Winnetwk.h:



#### RESOURCETYPE_ANY (0x00000000)

All resources



#### RESOURCETYPE_DISK (0x00000001)

Disk resources



#### RESOURCETYPE_PRINT (0x00000002)

Print resources


##### - dwType.RESOURCETYPE_ANY (0x00000000)

All resources


##### - dwType.RESOURCETYPE_DISK (0x00000001)

Disk resources


##### - dwType.RESOURCETYPE_PRINT (0x00000002)

Print resources

## -returns

Type: <b>HRESULT</b>

Always returns S_OK.

## -remarks

> [!NOTE]
> The shlobj_core.h header defines SHStartNetConnectionDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

