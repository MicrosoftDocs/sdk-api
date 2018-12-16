---
UID: NF:dwrite_3.IDWriteFontList1.GetFontLocality
title: IDWriteFontList1::GetFontLocality
author: windows-sdk-content
description: Gets the current location of a font given its zero-based index.
old-location: directwrite\idwritefontlist1_getfontlocality.htm
tech.root: DirectWrite
ms.assetid: A48641B8-0BFF-42B9-A093-A26404EC22C5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontLocality, GetFontLocality method [Direct Write], GetFontLocality method [Direct Write],IDWriteFontList1 interface, IDWriteFontList1 interface [Direct Write],GetFontLocality method, IDWriteFontList1.GetFontLocality, IDWriteFontList1::GetFontLocality, directwrite.idwritefontlist1_getfontlocality, dwrite_3/IDWriteFontList1::GetFontLocality
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
 - IDWriteFontList1.GetFontLocality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontList1::GetFontLocality


## -description


Gets the current location of a font given its zero-based index.


## -parameters




### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn890740(v=VS.85).aspx">DWRITE_LOCALITY</a></b>

Returns a <a href="https://msdn.microsoft.com/en-us/library/Dn890740(v=VS.85).aspx">DWRITE_LOCALITY</a>-typed value that specifies the location of the specified font.




## -remarks



For fully local files, the result will always be <b>DWRITE_LOCALITY_LOCAL</b>. For streamed files, the result depends on how much of the file has been downloaded. <a href="https://msdn.microsoft.com/en-us/library/Dn894595(v=VS.85).aspx">GetFont</a> fails if the locality is <b>DWRITE_LOCALITY_REMOTE</b> and potentially fails if <b>DWRITE_LOCALITY_PARTIAL</b>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894594(v=VS.85).aspx">IDWriteFontList1</a>
 

 

