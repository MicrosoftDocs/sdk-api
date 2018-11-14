---
UID: NF:dwrite.IDWriteTypography.GetFontFeature
title: IDWriteTypography::GetFontFeature
author: windows-sdk-content
description: Gets the font feature at the specified index.
old-location: directwrite\IDWriteTypography_GetFontFeature.htm
tech.root: DirectWrite
ms.assetid: deb6b466-a654-4bc7-863c-9db32aa4c036
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetFontFeature, GetFontFeature method [Direct Write], GetFontFeature method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],GetFontFeature method, IDWriteTypography.GetFontFeature, IDWriteTypography::GetFontFeature, directwrite.IDWriteTypography_GetFontFeature, dwrite/IDWriteTypography::GetFontFeature
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
 - IDWriteTypography.GetFontFeature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteTypography.GetFontFeature
: 
---

# IDWriteTypography::GetFontFeature


## -description


 Gets the font feature at the specified index.


## -parameters




### -param fontFeatureIndex

Type: <b>UINT32</b>

The zero-based index of the font feature to retrieve.


### -param fontFeature [out]

Type: <b><a href="https://msdn.microsoft.com/f8c2b1b0-ecab-4556-b3e6-5eda75e206ed">DWRITE_FONT_FEATURE</a>*</b>

When this method returns, contains the font feature which is at the specified index.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A single run of text can be associated with more than one typographic feature. The <a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a> object holds a list of these font features.




## -see-also




<a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>
 

 

