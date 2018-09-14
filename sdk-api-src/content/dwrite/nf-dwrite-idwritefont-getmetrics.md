---
UID: NF:dwrite.IDWriteFont.GetMetrics
title: IDWriteFont::GetMetrics
author: windows-sdk-content
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.
old-location: directwrite\IDWriteFont_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 0634d683-2c6e-40cb-94d9-2cf128fc3421
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetMetrics method, IDWriteFont.GetMetrics, IDWriteFont::GetMetrics, directwrite.IDWriteFont_GetMetrics, dwrite/IDWriteFont::GetMetrics
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
 - IDWriteFont.GetMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont::GetMetrics


## -description


 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.


## -parameters




### -param fontMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>*</b>

When this method returns, contains a structure that has font metrics for the current font face. The metrics returned by this function are in font design units.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

