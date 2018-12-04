---
UID: NF:mmiscapi.OpenDriver
title: OpenDriver function
author: windows-sdk-content
description: Opens an instance of an installable driver and initializes the instance using either the driver's default settings or a driver-specific value.
old-location: multimedia\opendriver.htm
tech.root: Multimedia
ms.assetid: 882146f7-cd42-45fd-8a5f-7078b64c7ea8
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: OpenDriver, OpenDriver function [Windows Multimedia], _win32_OpenDriver, mmsystem/OpenDriver, multimedia.opendriver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

32-bit driver-specific value. This value is passed as the <i>lParam2</i> parameter to the <a href="https://msdn.microsoft.com/d9a5535f-6b80-40cc-a20b-b7a342414d7f">DriverProc</a> function of the installable driver.


## -returns



Returns the handle of the installable driver instance if successful or <b>NULL</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/f3acbfa0-66d4-452b-b1df-ef6b46d1eb39">Installable Driver Functions</a>



<a href="https://msdn.microsoft.com/8b628a4d-48fa-4388-9d7c-0c901c45b7f3">Installable Drivers</a>
 

 

