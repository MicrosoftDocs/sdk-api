---
UID: NC:magnification.MagImageScalingCallback
title: MagImageScalingCallback
author: windows-sdk-content
description: Prototype for a callback function that implements a custom transform for image scaling.
old-location: magapi\magapi_MagImageScalingCallback.htm
old-project: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magimagescalingcallback.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: MagImageScalingCallback, MagImageScalingCallback callback, MagImageScalingCallback callback function [Magnification API], magapi.magapi_MagImageScalingCallback, magapi_MagImageScalingCallback, magnification/MagImageScalingCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Magnification.h
api_name:
-	MagImageScalingCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MagImageScalingCallback callback function


## -description


<div class="alert"><b>Note</b>  The <i>MagImageScalingCallback</i> function is deprecated in Windows 7 and later, and should not be used in new applications.  There is no alternate functionality.</div><div> </div>Prototype for a callback function that implements a custom transform for image scaling.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param *srcdata [in]

Type: <b>void*</b>

The input data.


### -param srcheader [in]

Type: <b><a href="https://msdn.microsoft.com/875a0e1d-2513-4ed2-8215-f2d2d91dd234">MAGIMAGEHEADER</a></b>

The description of the input format.


### -param *destdata [out]

Type: <b>void*</b>

The output data.


### -param destheader [in]

Type: <b><a href="https://msdn.microsoft.com/875a0e1d-2513-4ed2-8215-f2d2d91dd234">MAGIMAGEHEADER</a></b>

The description of the output format.


### -param unclipped [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The coordinates of the scaled version of the source bitmap.


### -param clipped [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The coordinates of the window to which the scaled bitmap is clipped.


### -param dirty [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRGN</a></b>

The region that needs to be refreshed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/875a0e1d-2513-4ed2-8215-f2d2d91dd234">MAGIMAGEHEADER</a>



<a href="https://msdn.microsoft.com/492a1022-503f-45ed-89e2-e2fe0d01bed6">MagGetImageScalingCallback</a>
 

 

