---
UID: NS:shlobj_core.CABINETSTATE
title: CABINETSTATE (shlobj_core.h)
description: CABINETSTATE may be altered or unavailable.
helpviewer_keywords: ["*LPCABINETSTATE","CABINETSTATE","CABINETSTATE structure [Windows Shell]","FALSE","SHCONTF_FOLDERS","SHCONTF_NONFOLDERS","TRUE","_win32_CABINETSTATE","shell.CABINETSTATE","shlobj_core/CABINETSTATE"]
old-location: shell\CABINETSTATE.htm
tech.root: shell
ms.assetid: 4b82b6a8-c4c0-4af2-9612-0551376c1c62
ms.date: 12/05/2018
ms.keywords: '*LPCABINETSTATE, CABINETSTATE, CABINETSTATE structure [Windows Shell], FALSE, SHCONTF_FOLDERS, SHCONTF_NONFOLDERS, TRUE, _win32_CABINETSTATE, shell.CABINETSTATE, shlobj_core/CABINETSTATE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CABINETSTATE, *LPCABINETSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPCABINETSTATE
 - shlobj_core/LPCABINETSTATE
 - CABINETSTATE
 - shlobj_core/CABINETSTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - CABINETSTATE
---

# CABINETSTATE structure


## -description

<p class="CCE_Message">[<b>CABINETSTATE</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Holds the global configuration for Windows Explorer and Windows Internet Explorer. This structure is used in the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-readcabinetstate">ReadCabinetState</a> and <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-writecabinetstate">WriteCabinetState</a> functions.

## -struct-fields

### -field cLength

Type: <b>WORD</b>

The size of the structure, in bytes.

### -field nVersion

Type: <b>WORD</b>

### -field fFullPathTitle

Type: <b>BOOL</b>



#### TRUE

Display the full path in the title bar.



#### FALSE

Display only the file name in the title bar.

### -field fSaveLocalView

Type: <b>BOOL</b>



#### TRUE

Remember each folder's view settings.



#### FALSE

Use global settings for all folders.

### -field fNotShell

Type: <b>BOOL</b>

Not used.

### -field fSimpleDefault

Type: <b>BOOL</b>

Not used.

### -field fDontShowDescBar

Type: <b>BOOL</b>

Not used.

### -field fNewWindowMode

Type: <b>BOOL</b>



#### TRUE

Display in a new window.



#### FALSE

Display in the current window.

### -field fShowCompColor

Type: <b>BOOL</b>



#### TRUE

Show encrypted or compressed NTFS files in color.



#### FALSE

Do not show encrypted or compressed NTFS files in color.

### -field fDontPrettyNames

Type: <b>BOOL</b>

Not used.

### -field fAdminsCreateCommonGroups

Type: <b>BOOL</b>

Used when an administrator installs an application that places an icon in the <b>Start</b> menu.



#### TRUE

Add the icon to the <b>Start</b> menu for all users (CSIDL_COMMON_STARTMENU). This is the default value.



#### FALSE

Add the icon to only the current user (CSIDL_STARTMENU).

### -field fUnusedFlags

Type: <b>UINT</b>

Not used.

### -field fMenuEnumFilter

Type: <b>UINT</b>

One or both of the following flags.



#### SHCONTF_FOLDERS

Display folders.



#### SHCONTF_NONFOLDERS

Display non-folder items.

