---
UID: NF:dwrite.IDWriteFontCollection.GetFontFromFontFace
title: IDWriteFontCollection::GetFontFromFontFace
author: windows-sdk-content
description: Gets the font object that corresponds to the same physical font as the specified font face object. The specified physical font must belong to the font collection.
old-location: directwrite\IDWriteFontCollection_GetFontFromFontFace.htm
tech.root: DirectWrite
ms.assetid: cc3c6cb9-9e98-4d45-bf73-ee625fb17e8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontFromFontFace, GetFontFromFontFace method [Direct Write], GetFontFromFontFace method [Direct Write],IDWriteFontCollection interface, IDWriteFontCollection interface [Direct Write],GetFontFromFontFace method, IDWriteFontCollection.GetFontFromFontFace, IDWriteFontCollection::GetFontFromFontFace, directwrite.IDWriteFontCollection_GetFontFromFontFace, dwrite/IDWriteFontCollection::GetFontFromFontFace
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
 - IDWriteFontCollection.GetFontFromFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontCollection::GetFontFromFontFace


## -description


 Gets the font object that corresponds to the same physical font as the specified font face object. The specified physical font must belong 
     to the font collection.


## -parameters




### -param fontFace

Type: <b><a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>*</b>

A font face object that specifies the physical font.


### -param font [out]

Type: <b><a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>**</b>

When this method returns, contains the address of a pointer to the newly created font object if successful; otherwise, <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>
 

 

