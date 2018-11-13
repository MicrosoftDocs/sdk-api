---
UID: NF:gdipluseffects.BrightnessContrast.SetParameters
title: BrightnessContrast::SetParameters
author: windows-sdk-content
description: The BrightnessContrast::SetParameters method sets the parameters of this BrightnessContrast object.
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrastclass\brightnesscontrastmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: BrightnessContrast class [GDI+],SetParameters method, BrightnessContrast.SetParameters, BrightnessContrast::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],BrightnessContrast class, _gdiplus_CLASS_BrightnessContrast_SetParameters_, gdiplus._gdiplus_CLASS_BrightnessContrast_SetParameters_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - BrightnessContrast.SetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# BrightnessContrast::SetParameters


## -description


The <b>BrightnessContrast::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/b5271911-7759-4e87-af25-7d9a9d9c653e">BrightnessContrastParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b5271911-7759-4e87-af25-7d9a9d9c653e">BrightnessContrastParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a>



<a href="https://msdn.microsoft.com/992feb3f-027a-45cd-8404-68f3a5a5999d">BrightnessContrast::GetParameters</a>
 

 

