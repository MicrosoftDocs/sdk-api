---
UID: NF:dwrite.IDWriteFontCollectionLoader.CreateEnumeratorFromKey
title: IDWriteFontCollectionLoader::CreateEnumeratorFromKey
author: windows-sdk-content
description: Creates a font file enumerator object that encapsulates a collection of font files. The font system calls back to this interface to create a font collection.
old-location: directwrite\IDWriteFontCollectionLoader_CreateEnumeratorFromKey.htm
tech.root: DirectWrite
ms.assetid: 579893e8-5ef3-4e23-a139-b5c203805c5c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateEnumeratorFromKey, CreateEnumeratorFromKey method [Direct Write], CreateEnumeratorFromKey method [Direct Write],IDWriteFontCollectionLoader interface, IDWriteFontCollectionLoader interface [Direct Write],CreateEnumeratorFromKey method, IDWriteFontCollectionLoader.CreateEnumeratorFromKey, IDWriteFontCollectionLoader::CreateEnumeratorFromKey, directwrite.IDWriteFontCollectionLoader_CreateEnumeratorFromKey, dwrite/IDWriteFontCollectionLoader::CreateEnumeratorFromKey
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
 - IDWriteFontCollectionLoader.CreateEnumeratorFromKey
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
- IDWriteFontCollectionLoader.CreateEnumeratorFromKey
: 
---

# IDWriteFontCollectionLoader::CreateEnumeratorFromKey


## -description


 Creates a font file enumerator object that encapsulates a collection of font files.
     The font system calls back to this interface to create a font collection.


## -parameters




### -param factory

Type: <b><a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a> object that was used to create the current font collection.


### -param collectionKey [in]

Type: <b>const void*</b>

A font collection key that uniquely identifies the collection of font files within
     the scope of the font collection loader being used. The buffer allocated for this key must be at least  the size, in bytes, specified by <i>collectionKeySize</i>.


### -param collectionKeySize

Type: <b>UINT32</b>

The size of the font collection key, in bytes.


### -param fontFileEnumerator [out]

Type: <b><a href="https://msdn.microsoft.com/d89efffd-ccda-4d55-8419-de142b0f9652">IDWriteFontFileEnumerator</a>**</b>

When this method returns, contains the address of  a pointer to the newly created font file enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a>
 

 

