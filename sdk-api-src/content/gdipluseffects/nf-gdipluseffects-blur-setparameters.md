---
UID: NF:gdipluseffects.Blur.SetParameters
title: Blur::SetParameters
author: windows-sdk-content
description: The Blur::SetParameters method sets the parameters of this Blur object.
old-location: gdiplus\_gdiplus_CLASS_Blur_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blurclass\blurmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Blur class [GDI+],SetParameters method, Blur.SetParameters, Blur::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],Blur class, _gdiplus_CLASS_Blur_SetParameters_, gdiplus._gdiplus_CLASS_Blur_SetParameters_
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
 - Blur.SetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Blur::SetParameters


## -description


The <b>Blur::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/en-us/library/ms534422(v=VS.85).aspx">Blur</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534057(v=VS.85).aspx">BlurParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534057(v=VS.85).aspx">BlurParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534422(v=VS.85).aspx">Blur</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536281(v=VS.85).aspx">Blur::GetParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534503(v=VS.85).aspx">Sharpen</a>
 

 

