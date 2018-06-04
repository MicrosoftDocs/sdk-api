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

# DwmSetPresentParameters function


## -description


Sets the present parameters for frame composition.
        
            

<b>DwmSetPresentParameters</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmSetPresentParameters</b> always return E_NOTIMPL.


## -parameters




### -param hwnd

The handle to the window where the present parameters are applied.


### -param pPresentParams [in, out]

A pointer to a <a href="https://msdn.microsoft.com/9fa736e7-9816-45e7-a864-da88403369b9">DWM_PRESENT_PARAMETERS</a> structure that contains DWM video frame parameters for frame composition.


## -returns



This function always returns S_OK.



