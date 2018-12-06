---
UID: NF:magnification.MagGetWindowTransform
title: MagGetWindowTransform function
author: windows-sdk-content
description: Retrieves the transformation matrix associated with a magnifier control.
old-location: magapi\magapi_MagGetWindowTransform.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowtransform.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MagGetWindowTransform, MagGetWindowTransform function [Magnification API], magapi.magapi_MagGetWindowTransform, magapi_MagGetWindowTransform, magnification/MagGetWindowTransform
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
 - MagGetWindowTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagGetWindowTransform function


## -description


Retrieves the transformation matrix associated with a magnifier control. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pTransform [out]

Type: <b><a href="https://msdn.microsoft.com/f07e64de-2fc8-4010-a5f1-b1ed29d06997">PMAGTRANSFORM</a></b>

The transformation matrix.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The transformation matrix specifies the magnification factor that the magnifier control applies to the contents of the source rectangle.




## -see-also




<a href="https://msdn.microsoft.com/2005f7de-5275-457e-a89f-794de5c66f5a">MagSetWindowTransform</a>
 

 

