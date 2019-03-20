---
UID: NF:dwrite.IDWriteFontFamily.GetFirstMatchingFont
title: IDWriteFontFamily::GetFirstMatchingFont (dwrite.h)
author: windows-sdk-content
description: Gets the font that best matches the specified properties.
old-location: directwrite\IDWriteFontFamily_GetFirstMatchingFont.htm
tech.root: DirectWrite
ms.assetid: ba5836a5-87ca-43bf-bb18-4498ed2a9619
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFirstMatchingFont, GetFirstMatchingFont method [Direct Write], GetFirstMatchingFont method [Direct Write],IDWriteFontFamily interface, IDWriteFontFamily interface [Direct Write],GetFirstMatchingFont method, IDWriteFontFamily.GetFirstMatchingFont, IDWriteFontFamily::GetFirstMatchingFont, directwrite.IDWriteFontFamily_GetFirstMatchingFont, dwrite/IDWriteFontFamily::GetFirstMatchingFont
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
 - IDWriteFontFamily.GetFirstMatchingFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFamily::GetFirstMatchingFont


## -description


 Gets the font that best matches the specified properties.


## -parameters




### -param weight

Type: <b><a href="https://msdn.microsoft.com/82396f80-eb62-4865-ba07-9653220c84f2">DWRITE_FONT_WEIGHT</a></b>

A value that is used to match a requested font weight.


### -param stretch

Type: <b><a href="https://msdn.microsoft.com/10b3a703-239b-4fb1-9a20-e466b123b060">DWRITE_FONT_STRETCH</a></b>

A value that is used to match a requested font stretch.


### -param style

Type: <b><a href="https://msdn.microsoft.com/e48a3b82-4a60-472d-8cb8-a6f63d7eeefc">DWRITE_FONT_STYLE</a></b>

A value that is used to match a requested font style.


### -param matchingFont [out]

Type: <b><a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>**</b>

When this method returns, contains the address of a pointer to the newly created <a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13">IDWriteFontFamily</a>
 

 

