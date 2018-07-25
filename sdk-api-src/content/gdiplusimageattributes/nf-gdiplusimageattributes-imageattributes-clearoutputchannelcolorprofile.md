---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearOutputChannelColorProfile
title: ImageAttributes::ClearOutputChannelColorProfile
author: windows-sdk-content
description: The ImageAttributes::ClearOutputChannelColorProfile method clears the output channel color profile setting for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearOutputChannelColorProfile_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearoutputchannelcolorprofile.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ClearOutputChannelColorProfile, ClearOutputChannelColorProfile method [GDI+], ClearOutputChannelColorProfile method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearOutputChannelColorProfile method, ImageAttributes.ClearOutputChannelColorProfile, ImageAttributes::ClearOutputChannelColorProfile, _gdiplus_CLASS_ImageAttributes_ClearOutputChannelColorProfile_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearOutputChannelColorProfile_type_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
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
 - ImageAttributes.ClearOutputChannelColorProfile
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearOutputChannelColorProfile


## -description


The <b>ImageAttributes::ClearOutputChannelColorProfile</b> method clears the output channel color profile setting for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the output channel profile setting is cleared. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify an output channel profile for the default category and a different output channel profile for the bitmap category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the bitmap category, then the default settings apply to the bitmap category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify an output channel profile and an adjustment matrix for the default category. If you set the output channel profile for the bitmap category by calling <a href="https://msdn.microsoft.com/b5e466d7-e2e1-471c-be05-a587b65556af">ImageAttributes::SetOutputChannelColorProfile</a>, then the default output channel profile will not apply to bitmaps. If you later clear the bitmap output channel profile by calling <b>ImageAttributes::ClearOutputChannelColorProfile</b>, the bitmap category will not revert to the default output channel profile; rather, the bitmap category will have no output channel profile setting. Similarly, the bitmap category will not revert to the default color-adjustment matrix; rather, the bitmap category will have no color-adjustment matrix.




## -see-also




<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/bb71bdc3-8ebe-4acd-959e-482037806598">ColorChannelFlags</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/63557a4a-834f-4914-8179-d66ca3585ecf">ImageAttributes::ClearOutputChannel</a>



<a href="https://msdn.microsoft.com/c84b0e5f-ab24-4693-811b-cfd2bbd8f85a">ImageAttributes::SetOutputChannel</a>



<a href="https://msdn.microsoft.com/b5e466d7-e2e1-471c-be05-a587b65556af">ImageAttributes::SetOutputChannelColorProfile</a>
 

 

