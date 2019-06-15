---
UID: NF:magnification.MagGetWindowTransform
title: MagGetWindowTransform function (magnification.h)
author: windows-sdk-content
description: Retrieves the transformation matrix associated with a magnifier control.
old-location: magapi\magapi_MagGetWindowTransform.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowtransform.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MagGetWindowTransform, MagGetWindowTransform function [Magnification API], magapi.magapi_MagGetWindowTransform, magapi_MagGetWindowTransform, magnification/MagGetWindowTransform
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
 - MagGetWindowTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MagGetWindowTransform function


## -description


Retrieves the transformation matrix associated with a magnifier control. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.


### -param pTransform [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/magnification/ns-magnification-tagmagtransform">PMAGTRANSFORM</a></b>

The transformation matrix.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The transformation matrix specifies the magnification factor that the magnifier control applies to the contents of the source rectangle.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetwindowtransform">MagSetWindowTransform</a>
 

 

