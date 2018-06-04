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

# DwmModifyPreviousDxFrameDuration function


## -description


Changes the number of monitor refreshes through which the previous frame will be displayed.
        
            

<b>DwmModifyPreviousDxFrameDuration</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmModifyPreviousDxFrameDuration</b> always return E_NOTIMPL.


## -parameters




### -param hwnd

The handle to the window for which the new duration is applied to the previous frame.


### -param cRefreshes

The number of refreshes to apply to the previous frame.


### -param fRelative

<b>TRUE</b> if the value given in <i>cRefreshes</i> is relative to the current value (added to or subtracted from it); <b>FALSE</b> if the value replaces the current value.


## -returns



This function always returns S_OK, even when DWM is not running.



