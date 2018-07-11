---
UID: NF:gdipluseffects.Blur.GetParameters
title: Blur::GetParameters
author: windows-sdk-content
description: The Blur::GetParameters method gets the current values of the parameters of this Blur object.
old-location: gdiplus\_gdiplus_CLASS_Blur_GetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blurclass\blurmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Blur class [GDI+],GetParameters method, Blur.GetParameters, Blur::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Blur class, _gdiplus_CLASS_Blur_GetParameters_, gdiplus._gdiplus_CLASS_Blur_GetParameters_
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
 - Blur.GetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Blur::GetParameters


## -description


The <b>Blur::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a>



<a href="https://msdn.microsoft.com/d5e62587-01f3-4869-a596-7e84d1752e37">Blur::SetParameters</a>



<a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a>
 

 

