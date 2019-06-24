---
UID: NL:gdiplusimaging.EncoderParameters
title: EncoderParameters (gdiplusimaging.h)
author: windows-sdk-content
description: An EncoderParameters object is an array of EncoderParameter objects along with a data member that specifies the number of EncoderParameter objects in the array.
old-location: gdiplus\_gdiplus_CLASS_EncoderParameters_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\encoderparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EncoderParameters, EncoderParameters class [GDI+], EncoderParameters class [GDI+],described, _gdiplus_CLASS_EncoderParameters_Class, gdiplus._gdiplus_CLASS_EncoderParameters_Class, gdiplusimaging/EncoderParameters
ms.topic: class
f1_keywords: ["gdiplusimaging/EncoderParameters"]
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - EncoderParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# EncoderParameters class


## -description


An <b>EncoderParameters</b> object is an array of <a href="https://docs.microsoft.com/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects along with a data member that specifies the number of <b>EncoderParameter</b> objects in the array.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">EncoderParameters</b> has these types of members:


## -remarks



When you create an <b>EncoderParameters</b> object, you must allocate enough memory to hold all of the <a href="https://docs.microsoft.com/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects that will eventually be placed in the array. For example, if you want to create an <b>EncoderParameters</b> object that will hold an array of five <b>EncoderParameter</b> objects, you should use code similar to the following:


```
EncoderParameters* pEncoderParameters = (EncoderParameters*)
   malloc(sizeof(EncoderParameters) + 4 * sizeof(EncoderParameter));
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-encoderparametervaluetype">EncoderParameterValueType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist">Image::GetEncoderParameterList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize">Image::GetEncoderParameterListSize</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
 

 

