---
UID: NF:dwrite.IDWriteFactory.CreateCustomFontCollection
title: IDWriteFactory::CreateCustomFontCollection
author: windows-sdk-content
description: Creates a font collection using a custom font collection loader.
old-location: directwrite\IDWriteFactory_CreateCustomFontCollection.htm
old-project: DirectWrite
ms.assetid: 983864bc-b737-4a4d-8f3f-f062eb88cfa7
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateCustomFontCollection, CreateCustomFontCollection method [Direct Write], CreateCustomFontCollection method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateCustomFontCollection method, IDWriteFactory.CreateCustomFontCollection, IDWriteFactory::CreateCustomFontCollection, directwrite.IDWriteFactory_CreateCustomFontCollection, dwrite/IDWriteFactory::CreateCustomFontCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory.CreateCustomFontCollection
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFactory::CreateCustomFontCollection


## -description


 Creates a font collection using a custom font collection loader.


## -parameters




### -param collectionLoader

Type: <b><a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a>*</b>

An application-defined font collection loader, which must have been previously
     registered using <a href="https://msdn.microsoft.com/495f8f56-42b6-4731-a26e-5da2c56a28ed">RegisterFontCollectionLoader</a>.


### -param collectionKey [in]

Type: <b>const void*</b>

The key used by the loader to identify a collection of font files.  The buffer allocated for this key should at least be the size of <i>collectionKeySize</i>.


### -param collectionKeySize

Type: <b>UINT32</b>

The size, in bytes, of the collection key.


### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>**</b>

Contains  an address of a pointer to the system font collection object if the method succeeds, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

