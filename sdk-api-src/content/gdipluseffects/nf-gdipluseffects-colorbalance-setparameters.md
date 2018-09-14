---
UID: NF:gdipluseffects.ColorBalance.SetParameters
title: ColorBalance::SetParameters
author: windows-sdk-content
description: The ColorBalance::SetParameters method sets the parameters of this ColorBalance object.
old-location: gdiplus\_gdiplus_CLASS_ColorBalance_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorbalanceclass\colorbalancemethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: ColorBalance class [GDI+],SetParameters method, ColorBalance.SetParameters, ColorBalance::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],ColorBalance class, _gdiplus_CLASS_ColorBalance_SetParameters_, gdiplus._gdiplus_CLASS_ColorBalance_SetParameters_
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
 - ColorBalance.SetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ColorBalance::SetParameters


## -description


The <b>ColorBalance::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a> object.


## -parameters




### -param parameters [in]

Type: <b><a href="https://msdn.microsoft.com/60e823da-d909-4e8c-ab2b-7f0d6d98620b">ColorBalanceParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/60e823da-d909-4e8c-ab2b-7f0d6d98620b">ColorBalanceParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a>



<a href="https://msdn.microsoft.com/94f13a9d-f831-4fa5-bea9-0fe675b91431">ColorBalance::GetParameters</a>
 

 

