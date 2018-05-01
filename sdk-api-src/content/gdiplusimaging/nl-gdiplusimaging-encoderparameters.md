---
UID: NL:gdiplusimaging.EncoderParameters
title: EncoderParameters
author: windows-driver-content
description: An EncoderParameters object is an array of EncoderParameter objects along with a data member that specifies the number of EncoderParameter objects in the array.
old-location: gdiplus\_gdiplus_CLASS_EncoderParameters_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\encoderparameters.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: EncoderParameters, EncoderParameters class [GDI+], EncoderParameters class [GDI+], described, _gdiplus_CLASS_EncoderParameters_Class, gdiplus._gdiplus_CLASS_EncoderParameters_Class, gdiplusimaging/EncoderParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdiplusimaging.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	EncoderParameters
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# EncoderParameters class


## -description


An <b>EncoderParameters</b> object is an array of <a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects along with a data member that specifies the number of <b>EncoderParameter</b> objects in the array.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">EncoderParameters</b> has these types of members:


## -remarks



When you create an <b>EncoderParameters</b> object, you must allocate enough memory to hold all of the <a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects that will eventually be placed in the array. For example, if you want to create an <b>EncoderParameters</b> object that will hold an array of five <b>EncoderParameter</b> objects, you should use code similar to the following:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>EncoderParameters* pEncoderParameters = (EncoderParameters*)
   malloc(sizeof(EncoderParameters) + 4 * sizeof(EncoderParameter));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/0ab532b0-0738-4cac-82d4-e2e25a955b2e">EncoderParameterValueType</a>



<a href="https://msdn.microsoft.com/2a7f40dc-1132-429b-bc44-79f28c9098d7">Image::GetEncoderParameterList</a>



<a href="https://msdn.microsoft.com/f7b0f80c-8fff-4fb7-bd7d-0b82275bd92d">Image::GetEncoderParameterListSize</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

