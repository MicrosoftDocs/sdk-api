---
UID: NF:dwrite.IDWriteTextFormat.GetTrimming
title: IDWriteTextFormat::GetTrimming
author: windows-sdk-content
description: Gets the trimming options for text that overflows the layout box.
old-location: directwrite\IDWriteTextFormat_GetTrimming.htm
old-project: DirectWrite
ms.assetid: 6147d0a4-8f50-40c6-864e-734cfef57089
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetTrimming, GetTrimming method [Direct Write], GetTrimming method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetTrimming method, IDWriteTextFormat.GetTrimming, IDWriteTextFormat::GetTrimming, directwrite.IDWriteTextFormat_GetTrimming, dwrite/IDWriteTextFormat::GetTrimming
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
 - IDWriteTextFormat.GetTrimming
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextFormat::GetTrimming


## -description


 Gets the trimming options for text that overflows the layout box.


## -parameters




### -param trimmingOptions [out]

Type: <b><a href="https://msdn.microsoft.com/c252b936-8a09-45b4-8138-84cf54058f72">DWRITE_TRIMMING</a>*</b>

When this method returns, it contains a pointer to a <a href="https://msdn.microsoft.com/c252b936-8a09-45b4-8138-84cf54058f72">DWRITE_TRIMMING</a> structure that holds the text trimming options for the overflowing text.


### -param trimmingSign [out]

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>**</b>

When this method returns, contains an address of a pointer to a trimming omission sign. This parameter may be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

