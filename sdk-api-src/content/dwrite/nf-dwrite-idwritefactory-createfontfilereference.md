---
UID: NF:dwrite.IDWriteFactory.CreateFontFileReference
title: IDWriteFactory::CreateFontFileReference (dwrite.h)
author: windows-sdk-content
description: Creates a font file reference object from a local font file.
old-location: directwrite\IDWriteFactory_CreateFontFileReference.htm
tech.root: DirectWrite
ms.assetid: ec67407d-e19b-4135-83ff-f3115e2da90c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFontFileReference, CreateFontFileReference method [Direct Write], CreateFontFileReference method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateFontFileReference method, IDWriteFactory.CreateFontFileReference, IDWriteFactory::CreateFontFileReference, directwrite.IDWriteFactory_CreateFontFileReference, dwrite/IDWriteFactory::CreateFontFileReference
ms.topic: method
f1_keywords: ["dwrite/IDWriteFactory.CreateFontFileReference"]
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFactory.CreateFontFileReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory::CreateFontFileReference


## -description


 Creates a font file reference object from a local font file.


## -parameters




### -param filePath [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the absolute file path for the font file. Subsequent operations on the constructed object may fail
     if the user provided <i>filePath</i> doesn't correspond to a valid file on the disk.


### -param lastWriteTime [in, optional]

Type: <b>const FILETIME*</b>

The last modified time of the input file path. If the parameter is omitted,
     the function will access the font file to obtain its last write time. You should specify this value
     to avoid extra disk access. Subsequent operations on the constructed object may fail
     if the user provided <i>lastWriteTime</i> doesn't match the file on the disk.


### -param fontFile [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

When this method returns, contains an address of a pointer to the newly created font file reference object, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>
 

 

