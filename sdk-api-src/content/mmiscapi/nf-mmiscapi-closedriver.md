---
UID: NF:mmiscapi.CloseDriver
title: CloseDriver function (mmiscapi.h)
description: Closes an installable driver.
helpviewer_keywords: ["CloseDriver","CloseDriver function [Windows Multimedia]","_win32_CloseDriver","mmsystem/CloseDriver","multimedia.closedriver"]
old-location: multimedia\closedriver.htm
tech.root: Multimedia
ms.assetid: 47d5c666-614d-4836-8e7d-0fe6b53d399f
ms.date: 12/05/2018
ms.keywords: CloseDriver, CloseDriver function [Windows Multimedia], _win32_CloseDriver, mmsystem/CloseDriver, multimedia.closedriver
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
 - CloseDriver
 - mmiscapi/CloseDriver
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
 - ext-ms-win-mf-winmm-l1-1-0.dll
api_name:
 - CloseDriver
---

# CloseDriver function


## -description

Closes an installable driver.

## -parameters

### -param hDriver [in]

Handle of an installable driver instance. The handle must have been previously created by using the <a href="/previous-versions/dd743639(v=vs.85)">OpenDriver</a> function.

### -param lParam1 [in]

32-bit driver-specific data.

### -param lParam2 [in]

32-bit driver-specific data.

## -returns

Returns nonzero if successful or zero otherwise.

## -remarks

The function passes the <i>lParam1</i> and <i>lParam2</i> parameters to the <a href="/previous-versions/dd797918(v=vs.85)">DriverProc</a> function of the installable driver.

## -see-also

<a href="/windows/desktop/Multimedia/installable-driver-functions">Installable Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>