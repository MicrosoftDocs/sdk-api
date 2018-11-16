---
UID: NF:dwrite.IDWriteFontFileLoader.CreateStreamFromKey
title: IDWriteFontFileLoader::CreateStreamFromKey
author: windows-sdk-content
description: Creates a font file stream object that encapsulates an open file resource.
old-location: directwrite\IDWriteFontFileLoader_CreateStreamFromKey.htm
tech.root: DirectWrite
ms.assetid: 1c0a7c7b-8201-45c5-ac46-20f0df034ccd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateStreamFromKey, CreateStreamFromKey method [Direct Write], CreateStreamFromKey method [Direct Write],IDWriteFontFileLoader interface, IDWriteFontFileLoader interface [Direct Write],CreateStreamFromKey method, IDWriteFontFileLoader.CreateStreamFromKey, IDWriteFontFileLoader::CreateStreamFromKey, directwrite.IDWriteFontFileLoader_CreateStreamFromKey, dwrite/IDWriteFontFileLoader::CreateStreamFromKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDWriteFontFileLoader.CreateStreamFromKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFontFileLoader.CreateStreamFromKey
: 
---

# IDWriteFontFileLoader::CreateStreamFromKey


## -description


 Creates a font file stream object that encapsulates an open file resource.
     


## -parameters




### -param fontFileReferenceKey [in]

Type: <b>const void*</b>

A pointer to a font file reference key that uniquely identifies the font file resource
     within the scope of the font loader being used. The buffer allocated for this key must at least be the size, in bytes, specified by <i> fontFileReferenceKeySize</i>.


### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

The size of font file reference key, in bytes.


### -param fontFileStream [out]

Type: <b><a href="https://msdn.microsoft.com/792ab9be-853f-427d-a762-2da8e81423f8">IDWriteFontFileStream</a>**</b>

When this method returns, contains the address of a pointer to the newly created <a href="https://msdn.microsoft.com/792ab9be-853f-427d-a762-2da8e81423f8">IDWriteFontFileStream</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The resource is closed when the last reference to <i>fontFileStream</i> is released.




## -see-also




<a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>
 

 

