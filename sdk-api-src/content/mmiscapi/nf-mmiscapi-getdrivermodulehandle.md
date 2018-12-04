---
UID: NF:mmiscapi.GetDriverModuleHandle
title: GetDriverModuleHandle function
author: windows-sdk-content
description: Retrieves the instance handle of the module that contains the installable driver.
old-location: multimedia\getdrivermodulehandle.htm
tech.root: Multimedia
ms.assetid: 13395864-f14f-4193-a451-4ac5f9830242
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GetDriverModuleHandle, GetDriverModuleHandle function [Windows Multimedia], _win32_GetDriverModuleHandle, mmsystem/GetDriverModuleHandle, multimedia.getdrivermodulehandle
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
 - GetDriverModuleHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDriverModuleHandle function


## -description


Retrieves the instance handle of the module that contains the installable driver.


## -parameters




### -param hDriver [in]

Handle of the installable driver instance. The handle must have been previously created by using the <a href="https://msdn.microsoft.com/882146f7-cd42-45fd-8a5f-7078b64c7ea8">OpenDriver</a> function.


## -returns



Returns an instance handle of the driver module if successful or <b>NULL</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/f3acbfa0-66d4-452b-b1df-ef6b46d1eb39">Installable Driver Functions</a>



<a href="https://msdn.microsoft.com/8b628a4d-48fa-4388-9d7c-0c901c45b7f3">Installable Drivers</a>
 

 

