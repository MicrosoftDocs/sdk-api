---
UID: NF:wincodec.IWICBitmapLock.GetSize
title: IWICBitmapLock::GetSize method
author: windows-driver-content
description: Retrieves the width and height, in pixels, of the locked rectangle.
old-location: wic\_wic_codec_iwicbitmaplock_getsize.htm
old-project: wic
ms.assetid: 355e81ec-d08a-464e-9b4e-fa8828e30406
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetSize method [Windows Imaging Component], GetSize method [Windows Imaging Component], IWICBitmapLock interface, GetSize,IWICBitmapLock.GetSize, IWICBitmapLock, IWICBitmapLock interface [Windows Imaging Component], GetSize method, IWICBitmapLock::GetSize, _wic_codec_iwicbitmaplock_getsize, wic._wic_codec_iwicbitmaplock_getsize, wincodec/IWICBitmapLock::GetSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapLock.GetSize
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapLock::GetSize method


## -description


Retrieves the width and height, in pixels, of the locked rectangle.


## -parameters




### -param puiWidth




### -param puiHeight






#### - pHeight [in, out]

Type: <b>UINT*</b>

A pointer that receives the height of the locked rectangle.


#### - pWidth [in, out]

Type: <b>UINT*</b>

A pointer that receives the width of the locked rectangle.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



