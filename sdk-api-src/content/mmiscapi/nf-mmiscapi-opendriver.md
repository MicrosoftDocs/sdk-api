---
UID: NF:mmiscapi.OpenDriver
title: OpenDriver function (mmiscapi.h)
description: Opens an instance of an installable driver and initializes the instance using either the driver's default settings or a driver-specific value.
helpviewer_keywords: ["OpenDriver","OpenDriver function [Windows Multimedia]","_win32_OpenDriver","mmsystem/OpenDriver","multimedia.opendriver"]
old-location: multimedia\opendriver.htm
tech.root: Multimedia
ms.assetid: 882146f7-cd42-45fd-8a5f-7078b64c7ea8
ms.date: 12/05/2018
ms.keywords: OpenDriver, OpenDriver function [Windows Multimedia], _win32_OpenDriver, mmsystem/OpenDriver, multimedia.opendriver
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
 - OpenDriver
 - mmiscapi/OpenDriver
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
 - OpenDriver
---

# OpenDriver function


## -description

Opens an instance of an installable driver and initializes the instance using either the driver's default settings or a driver-specific value.

## -parameters

### -param szDriverName [in]

Address of a null-terminated, wide-character string that specifies the filename of an installable driver or the name of a registry value associated with the installable driver. (This value must have been previously set when the driver was installed.)

### -param szSectionName [in]

Address of a null-terminated, wide-character string that specifies the name of the registry key containing the registry value given by the <i>lpDriverName</i> parameter. If <i>lpSectionName</i> is <b>NULL</b>, the registry key is assumed to be <b>Drivers32</b>.

### -param lParam2 [in]

32-bit driver-specific value. This value is passed as the <i>lParam2</i> parameter to the <a href="/previous-versions/dd797918(v=vs.85)">DriverProc</a> function of the installable driver.

## -returns

Returns the handle of the installable driver instance if successful or <b>NULL</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/installable-driver-functions">Installable Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>