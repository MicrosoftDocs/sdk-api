---
UID: NF:dwrite.IDWriteTypography.AddFontFeature
title: IDWriteTypography::AddFontFeature
author: windows-sdk-content
description: Adds an OpenType font feature.
old-location: directwrite\IDWriteTypography_AddFontFeature.htm
tech.root: DirectWrite
ms.assetid: 6d86a66d-a72f-4288-864f-90f877bd166d
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AddFontFeature, AddFontFeature method [Direct Write], AddFontFeature method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],AddFontFeature method, IDWriteTypography.AddFontFeature, IDWriteTypography::AddFontFeature, directwrite.IDWriteTypography_AddFontFeature, dwrite/IDWriteTypography::AddFontFeature
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
 - IDWriteTypography.AddFontFeature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTypography::AddFontFeature


## -description


 Adds an OpenType font feature.


## -parameters




### -param fontFeature [in]

Type: <b><a href="https://msdn.microsoft.com/f8c2b1b0-ecab-4556-b3e6-5eda75e206ed">DWRITE_FONT_FEATURE</a></b>

A structure that contains the OpenType name identifier and the execution parameter for the font feature being added.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>
 

 

