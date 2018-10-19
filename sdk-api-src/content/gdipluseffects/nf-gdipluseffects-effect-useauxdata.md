---
UID: NF:gdipluseffects.Effect.UseAuxData
title: Effect::UseAuxData
author: windows-sdk-content
description: The Effect::UseAuxData method sets or clears a flag that specifies whether the Bitmap::ApplyEffect method should return a pointer to the auxiliary data that it creates.
old-location: gdiplus\_gdiplus_CLASS_Effect_UseAuxData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\useauxdata.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: Effect class [GDI+],UseAuxData method, Effect.UseAuxData, Effect::UseAuxData, UseAuxData, UseAuxData method [GDI+], UseAuxData method [GDI+],Effect class, _gdiplus_CLASS_Effect_UseAuxData_, gdiplus._gdiplus_CLASS_Effect_UseAuxData_
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
 - Effect.UseAuxData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Effect::UseAuxData


## -description


The <b>Effect::UseAuxData</b> method sets or clears a flag that specifies whether the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates. 


## -parameters




### -param useAuxDataFlag [in]

Type: <b>const BOOL</b>

Set to <b>TRUE</b> to specify that <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">ApplyEffect</a> should return a pointer to its auxiliary data; <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534433(v=VS.85).aspx">Effect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536210(v=VS.85).aspx">Effect::GetAuxData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536211(v=VS.85).aspx">Effect::GetAuxDataSize</a>
 

 

