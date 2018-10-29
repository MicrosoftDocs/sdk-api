---
UID: NF:icm.CMDeleteTransform
title: CMDeleteTransform function
author: windows-sdk-content
description: The CMDeleteTransform function deletes a specified color transform, and frees any memory associated with it.
old-location: wcs\cmdeletetransform.htm
tech.root: WCS
ms.assetid: a9c2639e-d479-4067-afb8-5b5722a2cc60
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CMDeleteTransform, CMDeleteTransform function [Windows Color System], _color_CMDeleteTransform, icm/CMDeleteTransform, wcs.cmdeletetransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMDeleteTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMDeleteTransform function


## -description


The <b>CMDeleteTransform</b> function deletes a specified color transform, and frees any memory associated with it.


## -parameters




### -param hcmTransform

Identifies the color transform to be deleted.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. If the <b>CMDeleteTransform</b> function is not successful, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

