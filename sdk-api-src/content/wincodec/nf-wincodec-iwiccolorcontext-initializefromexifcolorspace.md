---
UID: NF:wincodec.IWICColorContext.InitializeFromExifColorSpace
title: IWICColorContext::InitializeFromExifColorSpace (wincodec.h)
description: Initializes the color context using an Exchangeable Image File (EXIF) color space.
helpviewer_keywords: ["IWICColorContext interface [Windows Imaging Component]","InitializeFromExifColorSpace method","IWICColorContext.InitializeFromExifColorSpace","IWICColorContext::InitializeFromExifColorSpace","InitializeFromExifColorSpace","InitializeFromExifColorSpace method [Windows Imaging Component]","InitializeFromExifColorSpace method [Windows Imaging Component]","IWICColorContext interface","_wic_codec_iwiccolorcontext_initializefromexifcolorspace","wic._wic_codec_iwiccolorcontext_initializefromexifcolorspace","wincodec/IWICColorContext::InitializeFromExifColorSpace"]
old-location: wic\_wic_codec_iwiccolorcontext_initializefromexifcolorspace.htm
tech.root: wic
ms.assetid: af85abf2-e1cc-4443-9726-a422ba363f71
ms.date: 12/05/2018
ms.keywords: IWICColorContext interface [Windows Imaging Component],InitializeFromExifColorSpace method, IWICColorContext.InitializeFromExifColorSpace, IWICColorContext::InitializeFromExifColorSpace, InitializeFromExifColorSpace, InitializeFromExifColorSpace method [Windows Imaging Component], InitializeFromExifColorSpace method [Windows Imaging Component],IWICColorContext interface, _wic_codec_iwiccolorcontext_initializefromexifcolorspace, wic._wic_codec_iwiccolorcontext_initializefromexifcolorspace, wincodec/IWICColorContext::InitializeFromExifColorSpace
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICColorContext::InitializeFromExifColorSpace
 - wincodec/IWICColorContext::InitializeFromExifColorSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICColorContext.InitializeFromExifColorSpace
---

# IWICColorContext::InitializeFromExifColorSpace


## -description

Initializes the color context using an Exchangeable Image File (EXIF) color space.

## -parameters

### -param value [in]

Type: <b>UINT</b>

The value of the EXIF color space.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A sRGB color space.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An Adobe RGB color space.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Once a color context has been initialized, it can't be re-initialized.

