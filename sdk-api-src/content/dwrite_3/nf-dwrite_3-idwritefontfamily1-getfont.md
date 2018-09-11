---
UID: NF:dwrite_3.IDWriteFontFamily1.GetFont
title: IDWriteFontFamily1::GetFont
author: windows-sdk-content
description: Gets a font given its zero-based index.
old-location: directwrite\idwritefontfamily1_getfont.htm
tech.root: DirectWrite
ms.assetid: B5C03AC5-E642-4AC8-94D1-D935BA159113
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetFont, GetFont method [Direct Write], GetFont method [Direct Write],IDWriteFontFamily1 interface, IDWriteFontFamily1 interface [Direct Write],GetFont method, IDWriteFontFamily1.GetFont, IDWriteFontFamily1::GetFont, directwrite.idwritefontfamily1_getfont, dwrite_3/IDWriteFontFamily1::GetFont
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFontFamily1.GetFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFamily1::GetFont


## -description


Gets a font given its zero-based index.


## -parameters




### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.


### -param font [out]

Type: <b><a href="https://msdn.microsoft.com/0BD21E3C-5F02-4A51-B64C-847B0DD5656B">IDWriteFont3</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/0BD21E3C-5F02-4A51-B64C-847B0DD5656B">IDWriteFont3</a> interface for the newly created font object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0642C2FA-03D0-4233-B8C4-27E4549B30BB">IDWriteFontFamily1</a>
 

 

