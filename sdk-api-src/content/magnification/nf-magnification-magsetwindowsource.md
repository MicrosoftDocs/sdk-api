---
UID: NF:magnification.MagSetWindowSource
title: MagSetWindowSource function
author: windows-sdk-content
description: Sets the source rectangle for the magnification window.
old-location: magapi\magapi_MagSetWindowSource.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetwindowsource.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MagSetWindowSource, MagSetWindowSource function [Magnification API], magapi.magapi_MagSetWindowSource, magapi_MagSetWindowSource, magnification/MagSetWindowSource
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
 - MagSetWindowSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagSetWindowSource function


## -description


Sets the source rectangle for the magnification window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param rect [in]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The rectangle to be magnified, in desktop coordinates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/eff56c0a-ef87-41e0-a94a-79f1ac3ab270">MagGetWindowSource</a>
 

 

