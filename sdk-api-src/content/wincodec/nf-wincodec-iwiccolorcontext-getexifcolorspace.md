---
UID: NF:wincodec.IWICColorContext.GetExifColorSpace
title: IWICColorContext::GetExifColorSpace (wincodec.h)
author: windows-sdk-content
description: Retrieves the Exchangeable Image File (EXIF) color space color context.
old-location: wic\_wic_codec_iwiccolorcontext_getexifcolorspace.htm
tech.root: wic
ms.assetid: ebd51090-fabb-4a6e-a77c-f1895bc27e54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetExifColorSpace, GetExifColorSpace method [Windows Imaging Component], GetExifColorSpace method [Windows Imaging Component],IWICColorContext interface, IWICColorContext interface [Windows Imaging Component],GetExifColorSpace method, IWICColorContext.GetExifColorSpace, IWICColorContext::GetExifColorSpace, _wic_codec_iwiccolorcontext_getexifcolorspace, wic._wic_codec_iwiccolorcontext_getexifcolorspace, wincodec/IWICColorContext::GetExifColorSpace
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICColorContext.GetExifColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICColorContext::GetExifColorSpace


## -description


Retrieves the Exchangeable Image File (EXIF) color space color context.


## -parameters




### -param pValue [out]

Type: <b>UINT*</b>

A pointer that receives the EXIF color space color context.

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
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>3 through 65534</dt>
</dl>
</td>
<td width="60%">
Unused.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should only be used when <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-gettype">IWICColorContext::GetType</a> indicates <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextExifColorSpace</a>.




