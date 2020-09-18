---
UID: NF:mmiscapi.DrvGetModuleHandle
title: DrvGetModuleHandle function (mmiscapi.h)
description: Retrieves the instance handle of the module that contains the installable driver. This function is provided for compatibility with previous versions of Windows.
helpviewer_keywords: ["DrvGetModuleHandle","DrvGetModuleHandle function [Windows Multimedia]","_win32_DrvGetModuleHandle","mmsystem/DrvGetModuleHandle","multimedia.drvgetmodulehandle"]
old-location: multimedia\drvgetmodulehandle.htm
tech.root: Multimedia
ms.assetid: 77246a9f-15fa-48a7-a4a8-9f7579b195c7
ms.date: 12/05/2018
ms.keywords: DrvGetModuleHandle, DrvGetModuleHandle function [Windows Multimedia], _win32_DrvGetModuleHandle, mmsystem/DrvGetModuleHandle, multimedia.drvgetmodulehandle
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
 - DrvGetModuleHandle
 - mmiscapi/DrvGetModuleHandle
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
 - DrvGetModuleHandle
---

# DrvGetModuleHandle function


## -description

Retrieves the instance handle of the module that contains the installable driver. This function is provided for compatibility with previous versions of Windows.

## -parameters

### -param hDriver [in]

Handle of the installable driver instance. The handle must have been previously created by using the <a href="/previous-versions/dd743639(v=vs.85)">OpenDriver</a> function.

## -returns

Returns an instance handle of the driver module if successful or <b>NULL</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/installable-driver-functions">Installable Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>