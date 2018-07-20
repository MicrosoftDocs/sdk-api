---
UID: NF:wincodec.IWICBitmapFrameDecode.GetThumbnail
title: IWICBitmapFrameDecode::GetThumbnail
author: windows-sdk-content
description: Retrieves a small preview of the frame, if supported by the codec.
old-location: wic\_wic_codec_iwicbitmapframedecode_getthumbnail.htm
old-project: wic
ms.assetid: 2792b54b-52d7-4205-a016-246a4dc5451d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetThumbnail, GetThumbnail method [Windows Imaging Component], GetThumbnail method [Windows Imaging Component],IWICBitmapFrameDecode interface, IWICBitmapFrameDecode interface [Windows Imaging Component],GetThumbnail method, IWICBitmapFrameDecode.GetThumbnail, IWICBitmapFrameDecode::GetThumbnail, _wic_codec_iwicbitmapframedecode_getthumbnail, wic._wic_codec_iwicbitmapframedecode_getthumbnail, wincodec/IWICBitmapFrameDecode::GetThumbnail
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameDecode.GetThumbnail
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameDecode::GetThumbnail


## -description


Retrieves a small preview of the frame, if supported by the codec.


## -parameters




### -param ppIThumbnail [out]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>**</b>

A pointer that receives a pointer to the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> of the thumbnail.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Not all formats support thumbnails. Joint Photographic Experts Group (JPEG), Tagged Image File Format (TIFF), and Microsoft Windows Digital Photo (WDP) support thumbnails.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
If the codec does not support thumbnails, return WINCODEC_ERROR_CODECNOTHUMBNAIL rather than E_NOTIMPL.



