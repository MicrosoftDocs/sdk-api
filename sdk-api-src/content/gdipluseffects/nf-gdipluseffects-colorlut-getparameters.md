---
UID: NF:gdipluseffects.ColorLUT.GetParameters
title: ColorLUT::GetParameters (gdipluseffects.h)
author: windows-sdk-content
description: The ColorLUT::GetParameters method gets the current values of the parameters of this ColorLUT object.
old-location: gdiplus\_gdiplus_CLASS_ColorLUT_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorlutclass\colorlutmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorLUT class [GDI+],GetParameters method, ColorLUT.GetParameters, ColorLUT::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorLUT class, _gdiplus_CLASS_ColorLUT_GetParameters_, gdiplus._gdiplus_CLASS_ColorLUT_GetParameters_
ms.topic: method
f1_keywords: ["gdipluseffects/ColorLUT.GetParameters"]
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
 - ColorLUT.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# ColorLUT::GetParameters


## -description


The <b>ColorLUT::GetParameters</b> method gets the current values of the parameters of this <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorlutparams">ColorLUTParams</a> structure.


### -param lut [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorlutparams">ColorLUTParams</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorlutparams">ColorLUTParams</a> structure that receives the parameter values.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorlut-setparameters">ColorLUT::SetParameters</a>
 

 

