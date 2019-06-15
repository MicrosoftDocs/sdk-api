---
UID: NN:wincodec.IWICColorContext
title: IWICColorContext (wincodec.h)
author: windows-sdk-content
description: Exposes methods for color management.
old-location: wic\_wic_codec_iwiccolorcontext.htm
tech.root: wic
ms.assetid: b6817676-affb-4bb3-adba-e24e0b75ad10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICColorContext, IWICColorContext interface [Windows Imaging Component], IWICColorContext interface [Windows Imaging Component],described, _wic_codec_iwiccolorcontext, wic._wic_codec_iwiccolorcontext, wincodec/IWICColorContext
ms.topic: interface
f1_keywords: ["wincodec/IWICColorContext"]
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
 - IWICColorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICColorContext interface


## -description


Exposes methods for color management.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICColorContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICColorContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICColorContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-getexifcolorspace">GetExifColorSpace</a>
</td>
<td align="left" width="63%">
Retrieves the EXIF color space color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-getprofilebytes">GetProfileBytes</a>
</td>
<td align="left" width="63%">
Retrieves the color context profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the color context type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-initializefromexifcolorspace">InitializeFromExifColorSpace</a>
</td>
<td align="left" width="63%">
Initializes the color context using an EXIF color space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-initializefromfilename">InitializeFromFilename</a>
</td>
<td align="left" width="63%">
Initializes the color context from the given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory">InitializeFromMemory</a>
</td>
<td align="left" width="63%">
Initializes the color context from a memory block.

</td>
</tr>
</table> 


## -remarks



A Color Context is an abstraction for a color profile. The profile can either be loaded from a file (like "sRGB Color Space Profile.icm"), read from a memory buffer, or can be defined by an EXIF color space. The system color profile directory can be obtained by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/getcolordirectory">GetColorDirectory</a>.

Once a color context has been initialized, it cannot be re-initialized.



