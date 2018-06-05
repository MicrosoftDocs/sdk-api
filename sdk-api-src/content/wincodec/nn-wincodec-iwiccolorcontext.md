---
UID: NN:wincodec.IWICColorContext
title: IWICColorContext
author: windows-sdk-content
description: Exposes methods for color management.
old-location: wic\_wic_codec_iwiccolorcontext.htm
old-project: wic
ms.assetid: b6817676-affb-4bb3-adba-e24e0b75ad10
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICColorContext, IWICColorContext interface [Windows Imaging Component], IWICColorContext interface [Windows Imaging Component],described, _wic_codec_iwiccolorcontext, wic._wic_codec_iwiccolorcontext, wincodec/IWICColorContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICColorContext
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICColorContext interface


## -description


Exposes methods for color management.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICColorContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICColorContext</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ebd51090-fabb-4a6e-a77c-f1895bc27e54">GetExifColorSpace</a>
</td>
<td align="left" width="63%">
Retrieves the EXIF color space color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59427a49-ef68-4680-b6d8-4ffa2a1913b8">GetProfileBytes</a>
</td>
<td align="left" width="63%">
Retrieves the color context profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the color context type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af85abf2-e1cc-4443-9726-a422ba363f71">InitializeFromExifColorSpace</a>
</td>
<td align="left" width="63%">
Initializes the color context using an EXIF color space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df1f841b-6b01-42d5-967d-47ec402f9b8c">InitializeFromFilename</a>
</td>
<td align="left" width="63%">
Initializes the color context from the given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cadc79b-85d0-495e-8309-8d5e3b246242">InitializeFromMemory</a>
</td>
<td align="left" width="63%">
Initializes the color context from a memory block.

</td>
</tr>
</table> 


## -remarks



A Color Context is an abstraction for a color profile. The profile can either be loaded from a file (like "sRGB Color Space Profile.icm"), read from a memory buffer, or can be defined by an EXIF color space. The system color profile directory can be obtained by calling <a href="https://msdn.microsoft.com/9e26e58b-0497-4879-963c-fae91f5740bf">GetColorDirectory</a>.

Once a color context has been initialized, it cannot be re-initialized.



