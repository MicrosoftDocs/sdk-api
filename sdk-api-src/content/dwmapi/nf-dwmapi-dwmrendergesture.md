---
UID: NF:dwmapi.DwmRenderGesture
title: DwmRenderGesture function (dwmapi.h)
author: windows-sdk-content
description: Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.
old-location: dwm\dwmrendergesture.htm
tech.root: dwm
ms.assetid: 2daad062-dd7f-4a0b-a31e-134980f5bebd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DwmRenderGesture, DwmRenderGesture function [Desktop Window Manager], dwm.dwmrendergesture, dwmapi/DwmRenderGesture
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
api_name:
 - DwmRenderGesture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DwmRenderGesture function


## -description


Notifies Desktop Window Manager (DWM) that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.


## -parameters




### -param arg1 [in]

The type of gesture, specified as one of the <a href="https://msdn.microsoft.com/3FBDDFC9-A3E7-43DC-B7C6-A23976861C28">GESTURE_TYPE</a> values.


### -param cContacts [in]

The number of contact points.


### -param pdwPointerID [in]

The pointer ID.


### -param pPoints [in]

The points.

