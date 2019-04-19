---
UID: NF:gdipluseffects.BrightnessContrast.GetParameters
title: BrightnessContrast::GetParameters (gdipluseffects.h)
author: windows-sdk-content
description: The BrightnessContrast::GetParameters method gets the current values of the parameters of this BrightnessContrast object.
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrastclass\brightnesscontrastmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BrightnessContrast class [GDI+],GetParameters method, BrightnessContrast.GetParameters, BrightnessContrast::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],BrightnessContrast class, _gdiplus_CLASS_BrightnessContrast_GetParameters_, gdiplus._gdiplus_CLASS_BrightnessContrast_GetParameters_
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
 - BrightnessContrast.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# BrightnessContrast::GetParameters


## -description


The <b>BrightnessContrast::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/en-us/library/ms534423(v=VS.85).aspx">BrightnessContrast</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/en-us/library/ms534058(v=VS.85).aspx">BrightnessContrastParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534058(v=VS.85).aspx">BrightnessContrastParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534058(v=VS.85).aspx">BrightnessContrastParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534423(v=VS.85).aspx">BrightnessContrast</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536278(v=VS.85).aspx">BrightnessContrast::SetParameters</a>
 

 

