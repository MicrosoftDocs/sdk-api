---
UID: NF:gdiplusheaders.FontFamily.FontFamily(IN const WCHAR,IN const FontCollection)
title: FontFamily::FontFamily(IN const WCHAR,IN const FontCollection)
author: windows-sdk-content
description: Creates a FontFamily::FontFamily object based on a specified font family.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilyconstructors\fontfamily_44name_fontcollection.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: FontFamily, FontFamily class [GDI+],FontFamily constructor, FontFamily constructor [GDI+], FontFamily constructor [GDI+],FontFamily class, FontFamily.FontFamily, FontFamily.FontFamily(IN const WCHAR,IN const FontCollection), FontFamily.FontFamily(const WCHAR*,const FontCollection*), FontFamily::FontFamily, FontFamily::FontFamily(IN const WCHAR,IN const FontCollection), _gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_, gdiplus._gdiplus_CLASS_FontFamily_FontFamily_name_fontCollection_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - FontFamily.FontFamily
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# FontFamily::FontFamily(IN const WCHAR,IN const FontCollection)


## -description


Creates a <b>FontFamily::FontFamily</b> object based on a specified font family.


## -parameters




### -param name [in]

Type: <b>const WCHAR*</b>

Name of the font family. For example, Arial.ttf is the name of the Arial font family. 


### -param fontCollection [in]

Type: <b>const <a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a>*</b>

Optional. Pointer to a 
					<a href="https://msdn.microsoft.com/5e1336ea-cb29-4fa4-85d5-077498a69cb2">FontCollection</a> object that specifies the collection that the font family belongs to. If 
					<b>FontCollection</b> is <b>NULL</b>, this font family is not part of a collection. The default value is <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>



<a href="https://msdn.microsoft.com/6c71a3eb-4fbf-45b0-ab35-8756a100af31">InstalledFontCollection</a>



<a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 

