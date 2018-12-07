---
UID: NF:dwrite.IDWriteGdiInterop.CreateFontFromLOGFONT
title: IDWriteGdiInterop::CreateFontFromLOGFONT
author: windows-sdk-content
description: Creates a font object that matches the properties specified by the LOGFONT structure.
old-location: directwrite\IDWriteGdiInterop_CreateFontFromLOGFONT.htm
tech.root: DirectWrite
ms.assetid: d083123a-1b45-4c18-9490-6ce038bb6b22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontFromLOGFONT, CreateFontFromLOGFONT method [Direct Write], CreateFontFromLOGFONT method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],CreateFontFromLOGFONT method, IDWriteGdiInterop.CreateFontFromLOGFONT, IDWriteGdiInterop::CreateFontFromLOGFONT, directwrite.IDWriteGdiInterop_CreateFontFromLOGFONT, dwrite/IDWriteGdiInterop::CreateFontFromLOGFONT
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
 - IDWriteGdiInterop.CreateFontFromLOGFONT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGdiInterop::CreateFontFromLOGFONT


## -description


 Creates a font object that matches the properties specified by the <b>LOGFONT</b> structure.


## -parameters




### -param logFont [in]

Type: <b>const LOGFONTW*</b>

A structure containing a GDI-compatible font description.


### -param font [out]

Type: <b><a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>**</b>

When this method returns, contains an address of a  pointer to a newly created <a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>  object if successful; otherwise, <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/79472021-ee12-45dd-a943-3908c9e06cde">IDWriteGdiInterop</a>
 

 

