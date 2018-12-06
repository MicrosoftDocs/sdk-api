---
UID: NF:dwrite.IDWriteTextFormat.GetFontCollection
title: IDWriteTextFormat::GetFontCollection
author: windows-sdk-content
description: Gets the current font collection.
old-location: directwrite\IDWriteTextFormat_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: a94cfca5-3a03-4912-9a33-df705a2265cf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetFontCollection method, IDWriteTextFormat.GetFontCollection, IDWriteTextFormat::GetFontCollection, directwrite.IDWriteTextFormat_GetFontCollection, dwrite/IDWriteTextFormat::GetFontCollection
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
 - IDWriteTextFormat.GetFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat::GetFontCollection


## -description


 Gets the current font collection.


## -parameters




### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>**</b>

When this method returns, contains an address of a pointer to the font collection being used for the current text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

