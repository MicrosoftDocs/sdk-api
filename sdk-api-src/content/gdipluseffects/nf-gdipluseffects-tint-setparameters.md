---
UID: NF:gdipluseffects.Tint.SetParameters
title: Tint::SetParameters
author: windows-sdk-content
description: The Tint::SetParameters method sets the parameters of this Tint object.
old-location: gdiplus\_gdiplus_CLASS_Tint_SetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tintclass\tintmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],Tint class, Tint class [GDI+],SetParameters method, Tint.SetParameters, Tint::SetParameters, _gdiplus_CLASS_Tint_SetParameters_, gdiplus._gdiplus_CLASS_Tint_SetParameters_
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
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - Tint.SetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Tint::SetParameters


## -description


The <b>Tint::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/library/ms534513(v=VS.85).aspx">Tint</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534074(v=VS.85).aspx">TintParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534074(v=VS.85).aspx">TintParams</a> object that specifies the parameters. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534513(v=VS.85).aspx">Tint</a>



<a href="https://msdn.microsoft.com/library/ms534517(v=VS.85).aspx">Tint::GetParameters</a>
 

 

