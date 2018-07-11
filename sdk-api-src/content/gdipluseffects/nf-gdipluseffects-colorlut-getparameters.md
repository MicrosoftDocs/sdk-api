---
UID: NF:gdipluseffects.ColorLUT.GetParameters
title: ColorLUT::GetParameters
author: windows-sdk-content
description: The ColorLUT::GetParameters method gets the current values of the parameters of this ColorLUT object.
old-location: gdiplus\_gdiplus_CLASS_ColorLUT_GetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorlutclass\colorlutmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ColorLUT class [GDI+],GetParameters method, ColorLUT.GetParameters, ColorLUT::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorLUT class, _gdiplus_CLASS_ColorLUT_GetParameters_, gdiplus._gdiplus_CLASS_ColorLUT_GetParameters_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ColorLUT::GetParameters


## -description


The <b>ColorLUT::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/library/ms534430(v=VS.85).aspx">ColorLUT</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/library/ms534061(v=VS.85).aspx">ColorLUTParams</a> structure.


### -param lut






#### - parameters [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms534061(v=VS.85).aspx">ColorLUTParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534061(v=VS.85).aspx">ColorLUTParams</a> structure that receives the parameter values.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534430(v=VS.85).aspx">ColorLUT</a>



<a href="https://msdn.microsoft.com/library/ms536237(v=VS.85).aspx">ColorLUT::SetParameters</a>
 

 

