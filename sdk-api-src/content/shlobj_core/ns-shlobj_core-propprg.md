---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PROPPRG structure


## -description


This structure contains information from a .pif file. It is used by <a href="https://msdn.microsoft.com/62933ddf-9b0d-427a-8b5f-a0117a3b4885">PifMgr_GetProperties</a>.


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

