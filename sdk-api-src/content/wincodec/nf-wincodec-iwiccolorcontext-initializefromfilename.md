---
UID: NF:wincodec.IWICColorContext.InitializeFromFilename
title: IWICColorContext::InitializeFromFilename (wincodec.h)
description: Initializes the color context from the given file.
helpviewer_keywords: ["IWICColorContext interface [Windows Imaging Component]","InitializeFromFilename method","IWICColorContext.InitializeFromFilename","IWICColorContext::InitializeFromFilename","InitializeFromFilename","InitializeFromFilename method [Windows Imaging Component]","InitializeFromFilename method [Windows Imaging Component]","IWICColorContext interface","_wic_codec_iwiccolorcontext_initializefromfilename","wic._wic_codec_iwiccolorcontext_initializefromfilename","wincodec/IWICColorContext::InitializeFromFilename"]
old-location: wic\_wic_codec_iwiccolorcontext_initializefromfilename.htm
tech.root: wic
ms.assetid: df1f841b-6b01-42d5-967d-47ec402f9b8c
ms.date: 12/05/2018
ms.keywords: IWICColorContext interface [Windows Imaging Component],InitializeFromFilename method, IWICColorContext.InitializeFromFilename, IWICColorContext::InitializeFromFilename, InitializeFromFilename, InitializeFromFilename method [Windows Imaging Component], InitializeFromFilename method [Windows Imaging Component],IWICColorContext interface, _wic_codec_iwiccolorcontext_initializefromfilename, wic._wic_codec_iwiccolorcontext_initializefromfilename, wincodec/IWICColorContext::InitializeFromFilename
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICColorContext::InitializeFromFilename
 - wincodec/IWICColorContext::InitializeFromFilename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICColorContext.InitializeFromFilename
---

# IWICColorContext::InitializeFromFilename


## -description

Initializes the color context from the given file.

## -parameters

### -param wzFilename [in]

Type: <b>LPCWSTR</b>

The name of the file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Once a color context has been initialized, it can't be re-initialized.

## -see-also

* [GetColorDirectoryW](/windows/win32/api/icm/nf-icm-getcolordirectoryw)
* [IWICColorContext](/windows/win32/api/wincodec/nn-wincodec-iwiccolorcontext)
