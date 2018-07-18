---
UID: NF:gdipluseffects.RedEyeCorrection.GetParameters
title: RedEyeCorrection::GetParameters
author: windows-sdk-content
description: The RedEyeCorrection::GetParameters method gets the current values of the parameters of this RedEyeCorrection object.
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_GetParameters_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrectionclass\redeyecorrectionmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],RedEyeCorrection class, RedEyeCorrection class [GDI+],GetParameters method, RedEyeCorrection.GetParameters, RedEyeCorrection::GetParameters, _gdiplus_CLASS_RedEyeCorrection_GetParameters_, gdiplus._gdiplus_CLASS_RedEyeCorrection_GetParameters_
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
 - RedEyeCorrection.GetParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# RedEyeCorrection::GetParameters


## -description


The <b>RedEyeCorrection::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object. 


## -parameters




### -param size [in]

Type: <b>UINT*</b>

The size, in bytes, of the buffer pointed to by the <i>parameters</i> parameter.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a>*</b>

Pointer to a buffer that is large enough to receive a <a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a> structure followed by an array of RECT structures. To determine the total size of the required buffer, call the GetParameterSize method of the <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object whose parameters you want to retrieve.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a>



<a href="https://msdn.microsoft.com/ed889acb-37c1-4fa6-9c46-1f41428b9b36">RedEyeCorrection::SetParameters</a>
 

 

