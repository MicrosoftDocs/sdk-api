---
UID: NF:magnification.MagSetWindowSource
title: MagSetWindowSource function
author: windows-sdk-content
description: Sets the source rectangle for the magnification window.
old-location: magapi\magapi_MagSetWindowSource.htm
old-project: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetwindowsource.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: MagSetWindowSource, MagSetWindowSource function [Magnification API], magapi.magapi_MagSetWindowSource, magapi_MagSetWindowSource, magnification/MagSetWindowSource
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
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
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
---

# MagSetWindowSource function


## -description


Sets the source rectangle for the magnification window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param rect [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The rectangle to be magnified, in desktop coordinates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/library/ms692390(v=VS.85).aspx">MagGetWindowSource</a>
 

 

