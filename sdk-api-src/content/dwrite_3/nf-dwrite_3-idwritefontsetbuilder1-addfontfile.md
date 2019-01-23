---
UID: NF:dwrite_3.IDWriteFontSetBuilder1.AddFontFile
title: IDWriteFontSetBuilder1::AddFontFile
author: windows-sdk-content
description: Adds references to all the fonts in the specified font file.
old-location: directwrite\idwritefontsetbuilder1_addfontfile.htm
tech.root: DirectWrite
ms.assetid: 3858EF37-F545-4C2E-BC3D-E4732B49911C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddFontFile, AddFontFile method [Direct Write], AddFontFile method [Direct Write],IDWriteFontSetBuilder1 interface, IDWriteFontSetBuilder1 interface [Direct Write],AddFontFile method, IDWriteFontSetBuilder1.AddFontFile, IDWriteFontSetBuilder1::AddFontFile, directwrite.idwritefontsetbuilder1_addfontfile, dwrite_3/IDWriteFontSetBuilder1::AddFontFile
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontSetBuilder1.AddFontFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontSetBuilder1::AddFontFile


## -description


Adds references to all the fonts in the specified font file.  The method parses the font file to determine the fonts and their properties.
      


## -parameters




### -param fontFile [in]

Type: <b>IDWriteFontFile*</b>

Font file reference object to add to the set. If the file is not a supported OpenType font file, then a DWRITE_E_FILEFORMAT error will be returned.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code. 




## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_font_data_loaded_into_memory">Creating a custom font set using font data loaded into memory</a>



<a href="directwrite.custom_font_sets_win10#creating_a_font_set_using_arbitrary_fonts_in_the_local_file_system">Creating a font set using arbitrary fonts in the local file system</a>



<a href="https://msdn.microsoft.com/32023D5C-5000-44A7-8C7A-995A821951BB">IDWriteFontSetBuilder1</a>
 

 

