---
UID: NF:gdipluseffects.Sharpen.GetParameters
title: Sharpen::GetParameters
author: windows-sdk-content
description: The Sharpen::GetParameters method gets the current values of the parameters of this Sharpen object.
old-location: gdiplus\_gdiplus_CLASS_Sharpen_GetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sharpenclass\sharpenmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Sharpen class, Sharpen class [GDI+],GetParameters method, Sharpen.GetParameters, Sharpen::GetParameters, _gdiplus_CLASS_Sharpen_GetParameters_, gdiplus._gdiplus_CLASS_Sharpen_GetParameters_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Sharpen.GetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Sharpen::GetParameters


## -description


The <b>Sharpen::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/9a3dd5ec-789b-4191-a680-6d85c12ab97b">SharpenParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/9a3dd5ec-789b-4191-a680-6d85c12ab97b">SharpenParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9a3dd5ec-789b-4191-a680-6d85c12ab97b">SharpenParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a>



<a href="https://msdn.microsoft.com/279fee59-6fcf-4a9d-b16e-e6de6b5977c1">Sharpen::SetParameters</a>
 

 

