---
UID: NF:gdipluseffects.Effect.GetParameterSize
title: Effect::GetParameterSize
author: windows-sdk-content
description: The Effect::GetParameterSize method gets the total size, in bytes, of the parameters currently set for this Effect. The Effect::GetParameterSize method is usually called on an object that is an instance of a descendant of the Effect class.
old-location: gdiplus\_gdiplus_CLASS_Effect_GetParameterSize_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\getparametersize.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: Effect class [GDI+],GetParameterSize method, Effect.GetParameterSize, Effect::GetParameterSize, GetParameterSize, GetParameterSize method [GDI+], GetParameterSize method [GDI+],Effect class, _gdiplus_CLASS_Effect_GetParameterSize_, gdiplus._gdiplus_CLASS_Effect_GetParameterSize_
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
 - Effect.GetParameterSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Effect::GetParameterSize


## -description


The <b>Effect::GetParameterSize</b> method  gets the total size, in bytes, of the parameters currently set for this <a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>. The <b>Effect::GetParameterSize</b> method is usually called on an object that is an instance of a descendant of the <b>Effect</b> class.


## -parameters




### -param size [out]

Type: <b>UINT*</b>

Pointer to a UINT that receives the total size of the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>



<a href="https://msdn.microsoft.com/ed889acb-37c1-4fa6-9c46-1f41428b9b36">SetParameters</a>
 

 

