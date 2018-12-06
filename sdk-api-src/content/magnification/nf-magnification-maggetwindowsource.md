---
UID: NF:magnification.MagGetWindowSource
title: MagGetWindowSource function
author: windows-sdk-content
description: Gets the rectangle of the area that is being magnified.
old-location: magapi\magapi_MagGetWindowSource.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowsource.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MagGetWindowSource, MagGetWindowSource function [Magnification API], magapi.magapi_MagGetWindowSource, magapi_MagGetWindowSource, magnification/MagGetWindowSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagGetWindowSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagGetWindowSource function


## -description


Gets the rectangle of the area that is being magnified.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pRect [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The rectangle that is being magnified, in desktop coordinates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/0f818905-e47b-48bf-867a-36f466bac56d">MagSetWindowSource</a>
 

 

