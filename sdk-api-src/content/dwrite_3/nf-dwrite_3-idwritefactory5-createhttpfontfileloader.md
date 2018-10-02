---
UID: NF:dwrite_3.IDWriteFactory5.CreateHttpFontFileLoader
title: IDWriteFactory5::CreateHttpFontFileLoader
author: windows-sdk-content
description: Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.
old-location: directwrite\idwritefactory5_createhttpfontfileloader.htm
tech.root: DirectWrite
ms.assetid: 7C8D581E-489D-48BE-8B3F-278E1C246BBA
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateHttpFontFileLoader, CreateHttpFontFileLoader method [Direct Write], CreateHttpFontFileLoader method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],CreateHttpFontFileLoader method, IDWriteFactory5.CreateHttpFontFileLoader, IDWriteFactory5::CreateHttpFontFileLoader, directwrite.idwritefactory5_createhttpfontfileloader, dwrite_3/IDWriteFactory5::CreateHttpFontFileLoader
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
 - IDWriteFactory5.CreateHttpFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory5::CreateHttpFontFileLoader


## -description


Creates a remote font file loader that can create font file references from HTTP or HTTPS URLs. The caller is responsible for registering and unregistering the loader.


## -parameters




### -param referrerUrl

Type: <b>wchar_t const*</b>

Optional referrer URL for HTTP requests.


### -param extraHeaders

Type: <b>wchar_t const*</b>

Optional additional header fields to include in HTTP requests. Each header field consists of a name followed by a colon (":") and the field value,
          as specified by RFC 2616. Multiple header fields may be separated by newlines.


### -param newLoader [out]

Type: <b><a href="https://msdn.microsoft.com/16CFF7ED-642A-48D8-8C72-3EC68B702E50">IDWriteRemoteFontFileLoader</a>**</b>

Receives a pointer to the newly-created loader object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_known_remote_fonts_on_the_Web">Creating a custom font set using known, remote fonts on the Web</a>



<a href="https://msdn.microsoft.com/2F3E30DC-A965-4C68-A337-73F338CF2563">IDWriteFactory5</a>
 

 

