---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontCollectionFromFontSet
title: IDWriteFactory3::CreateFontCollectionFromFontSet (dwrite_3.h)
author: windows-sdk-content
description: Create a weight/width/slope tree from a set of fonts.
old-location: directwrite\idwritefactory3_createfontcollectionfromfontset.htm
tech.root: DirectWrite
ms.assetid: 22cc005f-6d34-f701-ff83-63ba819ab651
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet method [Direct Write], CreateFontCollectionFromFontSet method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontCollectionFromFontSet method, IDWriteFactory3.CreateFontCollectionFromFontSet, IDWriteFactory3::CreateFontCollectionFromFontSet, directwrite.idwritefactory3_createfontcollectionfromfontset, dwrite_3/IDWriteFactory3::CreateFontCollectionFromFontSet
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
 - IDWriteFactory3.CreateFontCollectionFromFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::CreateFontCollectionFromFontSet


## -description


Create a weight/width/slope tree from a set of fonts.


## -parameters




### -param fontSet

Type: <b><a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>*</b>

A set of fonts to use to build the collection.


### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/bdee031b-53fa-321d-5cdc-4cc2c7ec58ca">IDWriteFontCollection1</a>**</b>

Holds the newly created font collection object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

