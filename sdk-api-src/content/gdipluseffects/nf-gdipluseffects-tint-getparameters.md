---
UID: NF:gdipluseffects.Tint.GetParameters
title: Tint::GetParameters
author: windows-sdk-content
description: The Tint::GetParameters method gets the current values of the parameters of this Tint object.
old-location: gdiplus\_gdiplus_CLASS_Tint_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tintclass\tintmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Tint class, Tint class [GDI+],GetParameters method, Tint.GetParameters, Tint::GetParameters, _gdiplus_CLASS_Tint_GetParameters_, gdiplus._gdiplus_CLASS_Tint_GetParameters_
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
 - Tint.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Tint::GetParameters


## -description


The <b>Tint::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/en-us/library/ms534513(v=VS.85).aspx">Tint</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/en-us/library/ms534074(v=VS.85).aspx">TintParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534074(v=VS.85).aspx">TintParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534074(v=VS.85).aspx">TintParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534513(v=VS.85).aspx">Tint</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534518(v=VS.85).aspx">Tint::SetParameters</a>
 

 

