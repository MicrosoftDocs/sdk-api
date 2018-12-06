---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl
title: IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl
author: windows-sdk-content
description: Creates a font file reference from a URL if the loader supports this capability.
old-location: directwrite\idwriteremotefontfileloader_createfontfilereferencefromurl.htm
tech.root: DirectWrite
ms.assetid: C8695514-532F-4CAC-9A50-049C81812F15
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontFileReferenceFromUrl, CreateFontFileReferenceFromUrl method [Direct Write], CreateFontFileReferenceFromUrl method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],CreateFontFileReferenceFromUrl method, IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl, IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl, directwrite.idwriteremotefontfileloader_createfontfilereferencefromurl, dwrite_3/IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteRemoteFontFileLoader.CreateFontFileReferenceFromUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRemoteFontFileLoader::CreateFontFileReferenceFromUrl


## -description


Creates a font file reference from a URL if the loader supports this capability.


## -parameters




### -param factory

Type: <b><a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>*</b>

Factory used to create the font file reference.


### -param baseUrl

Type: <b>WCHAR</b>

Optional base URL. The base URL is used to resolve the fontFileUrl if it is relative. For example, the baseUrl might be the URL of the referring document
          that contained the fontFileUrl.


### -param fontFileUrl [in]

Type: <b>WCHAR</b>

URL of the font resource.


### -param fontFile [out]

Type: <b><a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a>**</b>

Receives a pointer to the newly created font file reference.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



If baseUrl is a non-empty string, then baseUrl concatenated with fontFileUrl should form a valid URL, DirectWrite will not supply any additional delimiter.




## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_known_remote_fonts_on_the_Web">Creating a custom font set using known, remote fonts on the Web</a>



<a href="https://msdn.microsoft.com/16CFF7ED-642A-48D8-8C72-3EC68B702E50">IDWriteRemoteFontFileLoader</a>
 

 

