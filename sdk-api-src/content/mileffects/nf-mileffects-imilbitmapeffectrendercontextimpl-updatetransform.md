---
UID: NF:mileffects.IMILBitmapEffectRenderContextImpl.UpdateTransform
title: IMILBitmapEffectRenderContextImpl::UpdateTransform
author: windows-driver-content
description: Updates the output transform with the new matrix.
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl_updatetransform.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\updatetransform.htm
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],UpdateTransform method, IMILBitmapEffectRenderContextImpl.UpdateTransform, IMILBitmapEffectRenderContextImpl::UpdateTransform, UpdateTransform, UpdateTransform method [WPF Bitmap Effects], UpdateTransform method [WPF Bitmap Effects],IMILBitmapEffectRenderContextImpl interface, _wibe_imilbitmapeffectrendercontextimpl_updatetransform, mileffects/IMILBitmapEffectRenderContextImpl::UpdateTransform, wibe._wibe_imilbitmapeffectrendercontextimpl_updatetransform
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	Mileffects.dll
api_name:
-	IMILBitmapEffectRenderContextImpl.UpdateTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectRenderContextImpl::UpdateTransform


## -description


Updates the output transform with the new matrix.


## -parameters




### -param pMatrix [in]

Type: <b><a href="https://msdn.microsoft.com/b75a27b4-2aac-42a0-b45e-c9fc84655513">MILMatrixF</a>*</b>

The new transform to use.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



