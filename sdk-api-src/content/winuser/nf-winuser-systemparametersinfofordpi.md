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

# SystemParametersInfoForDpi function


## -description


Retrieves the value of one of the system-wide parameters, taking into account the provided DPI value.


## -parameters




### -param uiAction [in]

The system-wide parameter to be retrieved. This function is only intended for use with <b>SPI_GETICONTITLELOGFONT</b>, <b>SPI_GETICONMETRICS</b>, or <b>SPI_GETNONCLIENTMETRICS</b>. See <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> for more information on these values.


### -param uiParam [in]

A parameter whose usage and format depends on the system parameter being queried. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify zero for this parameter.


### -param pvParam [in, out]

A parameter whose usage and format depends on the system parameter being queried. For more information about system-wide parameters, see the <i>uiAction</i> parameter. If not otherwise indicated, you must specify <b>NULL</b> for this parameter. For information on the <b>PVOID</b> datatype, see <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>.


### -param fWinIni [in]

Has no effect for with this API. This parameter only has an effect if you're setting parameter.


### -param dpi [in]

The DPI to use for scaling the metric.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function returns a similar result as <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>, but scales it according to an arbitrary DPI you provide (if appropriate). It only scales with the following possible values for <i>uiAction</i>: <b>SPI_GETICONTITLELOGFONT</b>, <b>SPI_GETICONMETRICS</b>, <b>SPI_GETNONCLIENTMETRICS</b>. Other possible <i>uiAction</i> values do not provide ForDPI behavior, and therefore this function returns 0 if called with them.

For <i>uiAction</i> values that contain strings within their associated structures, only Unicode (<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONTW</a>) strings are supported in this function.



