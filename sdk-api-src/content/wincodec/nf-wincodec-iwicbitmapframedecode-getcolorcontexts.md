---
UID: NF:wincodec.IWICBitmapFrameDecode.GetColorContexts
title: IWICBitmapFrameDecode::GetColorContexts
author: windows-sdk-content
description: Retrieves the IWICColorContext associated with the image frame.
old-location: wic\_wic_codec_iwicbitmapframedecode_getcolorcontexts.htm
old-project: wic
ms.assetid: b869fc51-0f03-4f93-b5ad-805f9b216423
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetColorContexts, GetColorContexts method [Windows Imaging Component], GetColorContexts method [Windows Imaging Component],IWICBitmapFrameDecode interface, IWICBitmapFrameDecode interface [Windows Imaging Component],GetColorContexts method, IWICBitmapFrameDecode.GetColorContexts, IWICBitmapFrameDecode::GetColorContexts, _wic_codec_iwicbitmapframedecode_getcolorcontexts, wic._wic_codec_iwicbitmapframedecode_getcolorcontexts, wincodec/IWICBitmapFrameDecode::GetColorContexts
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameDecode.GetColorContexts
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameDecode::GetColorContexts


## -description


Retrieves the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> associated with the image frame.


## -parameters




### -param cCount [in]

Type: <b>UINT</b>

The number of color contexts to retrieve.

This value must be the size of, or smaller than, the size available to <i>ppIColorContexts</i>.


### -param ppIColorContexts [in, out]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

A pointer that receives a pointer to the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> objects.


### -param pcActualCount [out]

Type: <b>UINT*</b>

A pointer that receives the number of color contexts contained in the image frame.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If NULL is passed for <i>ppIColorContexts</i>, and 0 is passed for <i>cCount</i>, this method will return the total number of color contexts in the image in <i>pcActualCount</i>.



The <i>ppIColorContexts</i> array must be filled with valid data: each <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext*</a> in the array must have been created using <a href="https://msdn.microsoft.com/60ae0ec4-2bf4-43f0-9882-ff8b6f5f5923">IWICImagingFactory::CreateColorContext</a>.




