---
UID: NF:dwrite.IDWriteFont.GetFontFamily
title: IDWriteFont::GetFontFamily
author: windows-sdk-content
description: Gets the font family to which the specified font belongs.
old-location: directwrite\IDWriteFont_GetFontFamily.htm
tech.root: DirectWrite
ms.assetid: 6104a8ed-378f-4e2b-a0e5-8c0291750e65
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetFontFamily, GetFontFamily method [Direct Write], GetFontFamily method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetFontFamily method, IDWriteFont.GetFontFamily, IDWriteFont::GetFontFamily, directwrite.IDWriteFont_GetFontFamily, dwrite/IDWriteFont::GetFontFamily
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
 - IDWriteFont.GetFontFamily
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont::GetFontFamily


## -description


 Gets the font family to which the specified font belongs.


## -parameters




### -param fontFamily [out]

Type: <b><a href="https://msdn.microsoft.com/1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13">IDWriteFontFamily</a>**</b>

When this method returns, contains an address of a pointer to the font family object to which the specified font belongs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

