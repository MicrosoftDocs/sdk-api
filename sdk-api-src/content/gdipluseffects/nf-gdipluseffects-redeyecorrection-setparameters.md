---
UID: NF:gdipluseffects.RedEyeCorrection.SetParameters
title: RedEyeCorrection::SetParameters
author: windows-sdk-content
description: The RedEyeCorrection::SetParameters method sets the parameters of this RedEyeCorrection object.
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_SetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrectionclass\redeyecorrectionmethods\setparameters.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RedEyeCorrection class [GDI+],SetParameters method, RedEyeCorrection.SetParameters, RedEyeCorrection::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],RedEyeCorrection class, _gdiplus_CLASS_RedEyeCorrection_SetParameters_, gdiplus._gdiplus_CLASS_RedEyeCorrection_SetParameters_
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
 - RedEyeCorrection.SetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# RedEyeCorrection::SetParameters


## -description


The <b>RedEyeCorrection::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object.


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a>



<a href="https://msdn.microsoft.com/c7f57361-17ea-4188-bd8c-84e6e0f674ad">RedEyeCorrection::GetParameters</a>
 

 

