---
UID: NF:dwrite.IDWriteTextLayout.SetFontCollection
title: IDWriteTextLayout::SetFontCollection
author: windows-sdk-content
description: Sets the font collection.
old-location: directwrite\IDWriteTextLayout_SetFontCollection.htm
old-project: DirectWrite
ms.assetid: e80038bd-e157-4f76-85c7-559cadacb5c4
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontCollection method, IDWriteTextLayout.SetFontCollection, IDWriteTextLayout::SetFontCollection, SetFontCollection, SetFontCollection method [Direct Write], SetFontCollection method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontCollection, dwrite/IDWriteTextLayout::SetFontCollection
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
 - IDWriteTextLayout.SetFontCollection
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextLayout::SetFontCollection


## -description


 Sets the font collection.


## -parameters




### -param fontCollection

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>*</b>

The font collection to set.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

