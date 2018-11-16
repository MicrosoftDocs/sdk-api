---
UID: NF:gdiplusgraphics.Graphics.MeasureString(IN const WCHAR,IN INT,IN const Font,IN const PointF &,IN const StringFormat,OUT RectF)
title: Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const PointF &,IN const StringFormat,OUT RectF)
author: windows-sdk-content
description: The Graphics::MeasureString method measures the extent of the string in the specified font, format, and layout rectangle.
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureString_string_length_font_origin_stringFormat_boundingBox_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsmeasurestringmethods\measurestring_17string_length_font_origin_stringformat.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Graphics class [GDI+],MeasureString method, Graphics.MeasureString, Graphics.MeasureString(IN const WCHAR,IN INT,IN const Font,IN const PointF &,IN const StringFormat,OUT RectF), Graphics.MeasureString(const WCHAR*,INT,const Font*,const PointF&,const StringFormat*,RectF*), Graphics::MeasureString, Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const PointF &,IN const StringFormat,OUT RectF), MeasureString, MeasureString method [GDI+], MeasureString method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureString_string_length_font_origin_stringFormat_boundingBox_, gdiplus._gdiplus_CLASS_Graphics_MeasureString_string_length_font_origin_stringFormat_boundingBox_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.MeasureString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.MeasureString
: 
req.product: GDI+ 1.0
---

# Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const PointF &,IN const StringFormat,OUT RectF)


## -description


The <b>Graphics::MeasureString</b> method measures the extent of the string in the specified font, format, and layout rectangle.


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string to be measured. 

<div class="alert"><b>Important</b>  For bidirectional languages, such as Arabic, the string length must not exceed 2046 characters.</div>
<div> </div>

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters in the <i>string</i> array. The <i>length</i> parameter can be set to –1 if the string is null terminated. 


### -param font [in]

Type: <b>const <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a> object that specifies the family name, size, and style of the font that is applied to the string. 


### -param origin [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a></b>

Reference to the point at which the string starts. 


### -param stringFormat [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object that specifies the layout information, such as alignment, trimming, tab stops, and so forth. 


### -param boundingBox [out]

Type: <b><a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object that receives the rectangle that bounds the string. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns OK, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a>



<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>
 

 

