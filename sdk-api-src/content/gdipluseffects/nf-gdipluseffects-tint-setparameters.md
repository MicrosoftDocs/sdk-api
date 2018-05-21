---
UID: NF:gdipluseffects.Tint.SetParameters
title: Tint::SetParameters
author: windows-driver-content
description: The Tint::SetParameters method sets the parameters of this Tint object.
old-location: gdiplus\_gdiplus_CLASS_Tint_SetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tintclass\tintmethods\setparameters.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],Tint class, Tint class [GDI+],SetParameters method, Tint.SetParameters, Tint::SetParameters, _gdiplus_CLASS_Tint_SetParameters_, gdiplus._gdiplus_CLASS_Tint_SetParameters_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	Tint.SetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Tint::SetParameters


## -description


The <b>Tint::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/f012ec61-986d-40f4-a730-1b73a52952a8">Tint</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/d2d012d7-1e9e-4aea-a28c-df2d42ca1b69">TintParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d2d012d7-1e9e-4aea-a28c-df2d42ca1b69">TintParams</a> object that specifies the parameters. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f012ec61-986d-40f4-a730-1b73a52952a8">Tint</a>



<a href="https://msdn.microsoft.com/c4921fe2-40da-4805-b7c2-719e95fa767e">Tint::GetParameters</a>
 

 

