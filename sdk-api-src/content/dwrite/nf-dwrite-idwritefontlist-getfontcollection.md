---
UID: NF:dwrite.IDWriteFontList.GetFontCollection
title: IDWriteFontList::GetFontCollection (dwrite.h)
author: windows-sdk-content
description: Gets the font collection that contains the fonts in the font list.
old-location: directwrite\IDWriteFontList_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: f3c13a33-7bf7-4027-af10-f4863008cef2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteFontList interface, IDWriteFontList interface [Direct Write],GetFontCollection method, IDWriteFontList.GetFontCollection, IDWriteFontList::GetFontCollection, directwrite.IDWriteFontList_GetFontCollection, dwrite/IDWriteFontList::GetFontCollection
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
 - IDWriteFontList.GetFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontList::GetFontCollection


## -description


 Gets the font collection that contains the fonts in
    the font list.


## -parameters




### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>**</b>

When this method returns, contains the address of a pointer to the current <a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/00c41c5f-4405-45ff-98e5-03858dc3056f">IDWriteFontList</a>
 

 

