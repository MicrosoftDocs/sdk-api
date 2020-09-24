---
UID: NS:shlobj_core.PROPPRG
title: PROPPRG (shlobj_core.h)
description: This structure contains information from a .pif file. It is used by PifMgr_GetProperties.
helpviewer_keywords: ["*LPPROPPRG","*PPROPPRG","LPPROPPRG","LPPROPPRG structure pointer [Windows Properties]","PRGINIT_AMBIGUOUSPIF","PRGINIT_DEFAULT","PRGINIT_DEFAULTPIF","PRGINIT_INFSETTINGS","PRGINIT_INHIBITPIF","PRGINIT_MAXIMIZED","PRGINIT_MINIMIZED","PRGINIT_NOPIF","PRGINIT_REALMODE","PRGINIT_REALMODESILENT","PRG_CLOSEONEXIT","PRG_DEFAULT","PROPPRG","PROPPRG structure [Windows Properties]","RMOPT_CDROM","RMOPT_DISKLOCK","RMOPT_EMS","RMOPT_MOUSE","RMOPT_NETWORK","RMOPT_PRIVATECFG","RMOPT_VESA","_win32_PROPPRG","properties.PROPPRG","shell.PROPPRG","shlobj_core/LPPROPPRG","shlobj_core/PROPPRG"]
old-location: properties\PROPPRG.htm
tech.root: properties
ms.assetid: 603f990b-efb8-4d72-bc96-27bda4ffcbd8
ms.date: 12/05/2018
ms.keywords: '*LPPROPPRG, *PPROPPRG, LPPROPPRG, LPPROPPRG structure pointer [Windows Properties], PRGINIT_AMBIGUOUSPIF, PRGINIT_DEFAULT, PRGINIT_DEFAULTPIF, PRGINIT_INFSETTINGS, PRGINIT_INHIBITPIF, PRGINIT_MAXIMIZED, PRGINIT_MINIMIZED, PRGINIT_NOPIF, PRGINIT_REALMODE, PRGINIT_REALMODESILENT, PRG_CLOSEONEXIT, PRG_DEFAULT, PROPPRG, PROPPRG structure [Windows Properties], RMOPT_CDROM, RMOPT_DISKLOCK, RMOPT_EMS, RMOPT_MOUSE, RMOPT_NETWORK, RMOPT_PRIVATECFG, RMOPT_VESA, _win32_PROPPRG, properties.PROPPRG, shell.PROPPRG, shlobj_core/LPPROPPRG, shlobj_core/PROPPRG'
req.header: shlobj_core.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPPRG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPPRG
 - shlobj_core/PROPPRG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj_core.h
api_name:
 - PROPPRG
---

# PROPPRG structure


## -description

This structure contains information from a .pif file. It is used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_getproperties">PifMgr_GetProperties</a>.

## -struct-fields

### -field flPrg

Type: <b>WORD</b>

Flags that describe how the program will run.



#### PRG_DEFAULT

Use the default options.



#### PRG_CLOSEONEXIT

Close the application on exit.

### -field flPrgInit

Type: <b>WORD</b>

Flags that specify the initial conditions for the application.



#### PRGINIT_DEFAULT

Use the default options.



#### PRGINIT_MINIMIZED

The application should be minimized.



#### PRGINIT_MAXIMIZED

The application should be maximized.



#### PRGINIT_REALMODE

The application should run in real mode.



#### PRGINIT_REALMODESILENT

The application should run in real mode without being prompted.



#### PRGINIT_AMBIGUOUSPIF

The data is ambiguous.



#### PRGINIT_NOPIF

No .pif file was found.



#### PRGINIT_DEFAULTPIF

A default .pif was found.



#### PRGINIT_INFSETTINGS

A .inf file was found.



#### PRGINIT_INHIBITPIF

The .inf file indicates that a .pif file should not be created.

### -field achTitle

Type: <b>__wchar_t</b>

A null-terminated string that contains the title.

### -field achCmdLine

Type: <b>__wchar_t</b>

A null-terminated string that contains the command line, including arguments.

### -field achWorkDir

Type: <b>__wchar_t</b>

A null-terminated string that contains the working directory.

### -field wHotKey

Type: <b>WORD</b>

The key code of the .pif file's hotkey.

### -field achIconFile

Type: <b>__wchar_t</b>

A null-terminated string that contains the name of the file that contains the icon.

### -field wIconIndex

Type: <b>WORD</b>

The index of the icon in the file specified by <b>achIconFile</b>.

### -field dwEnhModeFlags

Type: <b>DWORD</b>

Reserved.

### -field dwRealModeFlags

Type: <b>DWORD</b>

Flags that specify the real mode options.



#### RMOPT_MOUSE

Requires a real-mode mouse.



#### RMOPT_EMS

Requires expanded memory.



#### RMOPT_CDROM

Requires CD-ROM support.



#### RMOPT_NETWORK

Requires network support.



#### RMOPT_DISKLOCK

Requires disk locking.



#### RMOPT_PRIVATECFG

Use a private config.sys or autoexec.bat file.



#### RMOPT_VESA

Requires a VESA driver.

### -field achOtherFile

Type: <b>__wchar_t</b>

A null-terminated string that contains the name of the "other" file in the directory.

### -field achPIFFile

Type: <b>__wchar_t</b>

A null-terminated string that contains the name of the .pif file in the directory.