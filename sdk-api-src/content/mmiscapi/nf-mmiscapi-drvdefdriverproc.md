---
UID: NF:mmiscapi.DrvDefDriverProc
title: DrvDefDriverProc function (mmiscapi.h)
description: Provides default processing for any messages not processed by an installable driver. This function is intended to be used only within the DriverProc function of an installable driver.D
helpviewer_keywords: ["DefDriverProc","DefDriverProc function [Windows Multimedia]","DrvDefDriverProc","_win32_DefDriverProc","mmsystem/DefDriverProc","multimedia.defdriverproc"]
old-location: multimedia\defdriverproc.htm
tech.root: Multimedia
ms.assetid: 8401925b-d286-41bd-b57e-838b2f5b250d
ms.date: 12/05/2018
ms.keywords: DefDriverProc, DefDriverProc function [Windows Multimedia], DrvDefDriverProc, _win32_DefDriverProc, mmsystem/DefDriverProc, multimedia.defdriverproc
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvDefDriverProc
 - mmiscapi/DrvDefDriverProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - DefDriverProc
---

# DrvDefDriverProc function


## -description

Provides default processing for any messages not processed by an installable driver. This function is intended to be used only within the <a href="/previous-versions/dd797918(v=vs.85)">DriverProc</a> function of an installable driver.

## -parameters

### -param dwDriverIdentifier

Identifier of the installable driver.

### -param hdrvr

Handle of the installable driver instance.

### -param uMsg

Driver message value.

### -param lParam1

32-bit message-dependent information.

### -param lParam2

32-bit message-dependent information.

## -returns

Returns nonzero if successful or zero otherwise.
