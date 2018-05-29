---
UID: NF:mileffects.IMILBitmapEffectPrimitive.GetOutput
title: IMILBitmapEffectPrimitive::GetOutput
author: windows-sdk-content
description: Performs pixel processing for the bitmap effect.
old-location: wibe\_wibe_imilbitmapeffectprimitive_getoutput.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\getoutput.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: GetOutput, GetOutput method [WPF Bitmap Effects], GetOutput method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],GetOutput method, IMILBitmapEffectPrimitive.GetOutput, IMILBitmapEffectPrimitive::GetOutput, _wibe_imilbitmapeffectprimitive_getoutput, mileffects/IMILBitmapEffectPrimitive::GetOutput, wibe._wibe_imilbitmapeffectprimitive_getoutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectPrimitive.GetOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitive::GetOutput


## -description


Performs pixel processing for the bitmap effect.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to use for output.


### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>*</b>

The render context to use to determine how the effect should be rendered.


### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether the effect should attempt to modify the input image in place.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

When this method returns, contains a pointer to the effect output.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            If <i>pfModifyInPlace</i> is VARIANT_TRUE, the input image may be modified and returned.
            If the custom effect does not support in place modifications, set <i>pfModifyInPlace</i> to VARIANT_FALSE to indicate a new image was created.
         



