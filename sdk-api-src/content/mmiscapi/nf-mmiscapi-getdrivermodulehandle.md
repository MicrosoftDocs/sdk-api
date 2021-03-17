---
UID: NF:mmiscapi.GetDriverModuleHandle
title: GetDriverModuleHandle function (mmiscapi.h)
description: Retrieves the instance handle of the module that contains the installable driver.
helpviewer_keywords: ["GetDriverModuleHandle","GetDriverModuleHandle function [Windows Multimedia]","_win32_GetDriverModuleHandle","mmsystem/GetDriverModuleHandle","multimedia.getdrivermodulehandle"]
old-location: multimedia\getdrivermodulehandle.htm
tech.root: Multimedia
ms.assetid: 13395864-f14f-4193-a451-4ac5f9830242
ms.date: 12/05/2018
ms.keywords: GetDriverModuleHandle, GetDriverModuleHandle function [Windows Multimedia], _win32_GetDriverModuleHandle, mmsystem/GetDriverModuleHandle, multimedia.getdrivermodulehandle
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Installable Drivers, Installable Driver Functions
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
 - GetDriverModuleHandle
 - mmiscapi/GetDriverModuleHandle
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
 - GetDriverModuleHandle
---

# GetDriverModuleHandle function


## -description

Retrieves the instance handle of the module that contains the installable driver.

## -parameters

### -param hDriver [in]

Handle of the installable driver instance. The handle must have been previously created by using the <a href="/previous-versions/dd743639(v=vs.85)">OpenDriver</a> function.

## -returns

Returns an instance handle of the driver module if successful or <b>NULL</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/installable-driver-functions">Installable Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>