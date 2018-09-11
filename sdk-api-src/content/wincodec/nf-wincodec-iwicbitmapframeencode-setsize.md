---
UID: NF:wincodec.IWICBitmapFrameEncode.SetSize
title: IWICBitmapFrameEncode::SetSize
author: windows-sdk-content
description: Sets the output image dimensions for the frame.
old-location: wic\_wic_codec_iwicbitmapframeencode_setsize.htm
tech.root: wic
ms.assetid: e21e1a66-b1fa-4700-a14e-dc382b5404f7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetSize method, IWICBitmapFrameEncode.SetSize, IWICBitmapFrameEncode::SetSize, SetSize, SetSize method [Windows Imaging Component], SetSize method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setsize, wic._wic_codec_iwicbitmapframeencode_setsize, wincodec/IWICBitmapFrameEncode::SetSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode.SetSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapFrameEncode::SetSize


## -description


Sets the output image dimensions for the frame.


## -parameters




### -param uiWidth [in]

Type: <b>UINT</b>

The width of the output image.


### -param uiHeight [in]

Type: <b>UINT</b>

The height of the output image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



