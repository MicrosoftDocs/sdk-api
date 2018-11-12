---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontFaceReference(WCHAR const,FILETIME const,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference)
title: IDWriteFactory3::CreateFontFaceReference(WCHAR const,FILETIME const,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference)
author: windows-sdk-content
description: Creates a reference to a font given a full path.
old-location: directwrite\idwritefactory3_createfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 3ae2150b-af56-65f5-fe38-7ecea16cf0b8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateFontFaceReference, CreateFontFaceReference method [Direct Write], CreateFontFaceReference method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontFaceReference method, IDWriteFactory3.CreateFontFaceReference, IDWriteFactory3.CreateFontFaceReference(WCHAR const,FILETIME const,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference), IDWriteFactory3::CreateFontFaceReference, IDWriteFactory3::CreateFontFaceReference(WCHAR const,FILETIME const,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference), directwrite.idwritefactory3_createfontfacereference, dwrite_3/IDWriteFactory3::CreateFontFaceReference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory3.CreateFontFaceReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::CreateFontFaceReference(WCHAR const,FILETIME const,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference)


## -description


Creates a reference to a font given a full path. 


## -parameters




#### - filePath [in]

Type: <b>WCHAR</b>

Absolute file path. Subsequent operations on the constructed object may fail      
          if the user provided filePath doesn't correspond to a valid file on the disk.


#### - lastWriteTime [in, optional]

Type: <b>FILETIME</b>

Last modified time of the input file path. If the parameter is omitted,      
          the function will access the font file to obtain its last write time, so the clients are encouraged to specify this value      
          to avoid extra disk access. Subsequent operations on the constructed object may fail      
          if the user provided lastWriteTime doesn't match the file on the disk.


### -param faceIndex

Type: <b>UINT32</b>

The zero based index of a font face in cases when the font files contain a collection of font faces.      
          If the font files contain a single face, this value should be zero.


### -param fontSimulations

Type: <b><a href="https://msdn.microsoft.com/0881afec-2fa5-4f17-96a2-68a5293e0bba">DWRITE_FONT_SIMULATIONS</a></b>

Font face simulation flags for algorithmic emboldening and italicization.


### -param fontFaceReference [out]

Type: <b><a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>**</b>

Contains newly created font face reference object, or nullptr in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

