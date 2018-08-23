---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearOutputChannel
title: ImageAttributes::ClearOutputChannel
author: windows-sdk-content
description: The ImageAttributes::ClearOutputChannel method clears the cyan-magenta-yellow-black (CMYK) output channel setting for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearoutputchannel.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ClearOutputChannel, ClearOutputChannel method [GDI+], ClearOutputChannel method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearOutputChannel method, ImageAttributes.ClearOutputChannel, ImageAttributes::ClearOutputChannel, _gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.ClearOutputChannel
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearOutputChannel


## -description


The <b>ImageAttributes::ClearOutputChannel</b> method clears the cyan-magenta-yellow-black (CMYK) output channel setting for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the output channel setting is cleared. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify an output channel for the default category and a different output channel for the bitmap category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the bitmap category, then the default settings apply to the bitmap category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify an output channel and an adjustment matrix for the default category. If you set the output channel for the bitmap category by calling <a href="https://msdn.microsoft.com/en-us/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a>, then the default output channel will not apply to bitmaps. If you later clear the bitmap output channel by calling <b>ImageAttributes::ClearOutputChannel</b>, the bitmap category will not revert to the default output channel; rather, the bitmap category will have no output channel setting. Similarly, the bitmap category will not revert to the default color-adjustment matrix; rather, the bitmap category will have no color-adjustment matrix.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534090(v=VS.85).aspx">ColorChannelFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535421(v=VS.85).aspx">ImageAttributes::ClearOutputChannelColorProfile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535434(v=VS.85).aspx">ImageAttributes::SetOutputChannel</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535435(v=VS.85).aspx">ImageAttributes::SetOutputChannelColorProfile</a>
 

 

