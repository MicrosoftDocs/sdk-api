---
UID: NF:dwrite.IDWriteTypography.GetFontFeatureCount
title: IDWriteTypography::GetFontFeatureCount
author: windows-sdk-content
description: Gets the number of OpenType font features for the current font.
old-location: directwrite\IDWriteTypography_GetFontFeatureCount.htm
old-project: DirectWrite
ms.assetid: 434ea913-00c9-4051-b13c-68f9d67ebd84
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFontFeatureCount, GetFontFeatureCount method [Direct Write], GetFontFeatureCount method [Direct Write],IDWriteTypography interface, IDWriteTypography interface [Direct Write],GetFontFeatureCount method, IDWriteTypography.GetFontFeatureCount, IDWriteTypography::GetFontFeatureCount, directwrite.IDWriteTypography_GetFontFeatureCount, dwrite/IDWriteTypography::GetFontFeatureCount
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
 - IDWriteTypography.GetFontFeatureCount
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTypography::GetFontFeatureCount


## -description


 Gets the number of OpenType font features for the current font.


## -parameters






## -returns



Type: <b>UINT32</b>

The number of font features for the current text format.




## -remarks



A single run of text can be associated with more than one typographic feature. The <a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a> object holds a list of these font features.




## -see-also




<a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>
 

 

