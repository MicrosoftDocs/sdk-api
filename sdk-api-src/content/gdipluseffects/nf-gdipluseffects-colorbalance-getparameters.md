---
UID: NF:gdipluseffects.ColorBalance.GetParameters
title: ColorBalance::GetParameters
author: windows-driver-content
description: The ColorBalance::GetParameters method gets the current values of the parameters of this ColorBalance object.
old-location: gdiplus\_gdiplus_CLASS_ColorBalance_GetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorbalanceclass\colorbalancemethods\getparameters.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ColorBalance class [GDI+],GetParameters method, ColorBalance.GetParameters, ColorBalance::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorBalance class, _gdiplus_CLASS_ColorBalance_GetParameters_, gdiplus._gdiplus_CLASS_ColorBalance_GetParameters_
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
-	Gdiplus.dll
api_name:
-	ColorBalance.GetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ColorBalance::GetParameters


## -description


The <b>ColorBalance::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/60e823da-d909-4e8c-ab2b-7f0d6d98620b">ColorBalanceParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/60e823da-d909-4e8c-ab2b-7f0d6d98620b">ColorBalanceParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/60e823da-d909-4e8c-ab2b-7f0d6d98620b">ColorBalanceParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a>



<a href="https://msdn.microsoft.com/5e2cc043-c3da-428e-b7a0-f2ad8a1eefbe">ColorBalance::SetParameters</a>
 

 

