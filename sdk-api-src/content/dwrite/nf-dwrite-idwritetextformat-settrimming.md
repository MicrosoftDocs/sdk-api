---
UID: NF:dwrite.IDWriteTextFormat.SetTrimming
title: IDWriteTextFormat::SetTrimming
author: windows-sdk-content
description: Sets trimming options for text overflowing the layout width.
old-location: directwrite\IDWriteTextFormat_SetTrimming.htm
tech.root: DirectWrite
ms.assetid: 737eab93-2761-4a59-81e8-ef827be30325
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetTrimming method, IDWriteTextFormat.SetTrimming, IDWriteTextFormat::SetTrimming, SetTrimming, SetTrimming method [Direct Write], SetTrimming method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetTrimming, dwrite/IDWriteTextFormat::SetTrimming
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
 - IDWriteTextFormat.SetTrimming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat::SetTrimming


## -description


 Sets trimming options for text overflowing the layout width.


## -parameters




### -param trimmingOptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/c252b936-8a09-45b4-8138-84cf54058f72">DWRITE_TRIMMING</a>*</b>

Text trimming options.


### -param trimmingSign

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>*</b>

Application-defined omission sign. This parameter may be <b>NULL</b>. See <a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a> for more information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

