---
UID: NF:dwrite.IDWriteTextLayout.GetFontStyle
title: IDWriteTextLayout::GetFontStyle
author: windows-sdk-content
description: Gets the font style (also known as slope) of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetFontStyle.htm
old-project: DirectWrite
ms.assetid: 184aa6c8-4dc5-4881-a0e0-61dc0b1a8240
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFontStyle, GetFontStyle method [Direct Write], GetFontStyle method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontStyle method, IDWriteTextLayout.GetFontStyle, IDWriteTextLayout::GetFontStyle, directwrite.IDWriteTextLayout_GetFontStyle, dwrite/IDWriteTextLayout::GetFontStyle
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
 - IDWriteTextLayout.GetFontStyle
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextLayout::GetFontStyle


## -description


 Gets the font style (also known as slope) of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.


### -param fontStyle [out]

Type: <b><a href="https://msdn.microsoft.com/e48a3b82-4a60-472d-8cb8-a6f63d7eeefc">DWRITE_FONT_STYLE</a>*</b>

When this method returns, contains a value which indicates the type of font style (also known as slope or incline) being applied at the specified position.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font style.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

