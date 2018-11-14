---
UID: NF:gdipluseffects.Blur.SetParameters
title: Blur::SetParameters
author: windows-sdk-content
description: The Blur::SetParameters method sets the parameters of this Blur object.
old-location: gdiplus\_gdiplus_CLASS_Blur_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blurclass\blurmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
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
- apiref
: 
- COM
: 
- gdipluseffects.h
: 
- Blur.SetParameters
: 
req.product: GDI+ 1.1
---

# Blur::SetParameters


## -description


The <b>Blur::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a>



<a href="https://msdn.microsoft.com/efabf84d-f4f9-4686-9d26-c2ca0239ac2c">Blur::GetParameters</a>



<a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a>
 

 

