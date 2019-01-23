---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontSetBuilder
title: IDWriteFactory3::CreateFontSetBuilder
author: windows-sdk-content
description: Creates an empty font set builder to add font face references and create a custom font set.
old-location: directwrite\idwritefactory3_createfontsetbuilder.htm
tech.root: DirectWrite
ms.assetid: 8021f934-af83-ccd0-e142-455df88bf936
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontSetBuilder, CreateFontSetBuilder method [Direct Write], CreateFontSetBuilder method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontSetBuilder method, IDWriteFactory3.CreateFontSetBuilder, IDWriteFactory3::CreateFontSetBuilder, directwrite.idwritefactory3_createfontsetbuilder, dwrite_3/IDWriteFactory3::CreateFontSetBuilder
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
 - IDWriteFactory3.CreateFontSetBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::CreateFontSetBuilder


## -description


Creates an empty font set builder to add font face references     
  and create a custom font set. 


## -parameters




### -param fontSetBuilder [out]

Type: <b><a href="https://msdn.microsoft.com/CC6C95CA-BA8B-47C4-A241-650EC8477192">IDWriteFontSetBuilder</a>**</b>

Holds the newly created font set builder object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

