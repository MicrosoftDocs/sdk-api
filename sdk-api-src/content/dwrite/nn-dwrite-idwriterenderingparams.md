---
UID: NN:dwrite.IDWriteRenderingParams
title: IDWriteRenderingParams (dwrite.h)
description: Represents text rendering settings such as ClearType level, enhanced contrast, and gamma correction for glyph rasterization and filtering.
helpviewer_keywords: ["IDWriteRenderingParams","IDWriteRenderingParams interface [Direct Write]","IDWriteRenderingParams interface [Direct Write]","described","directwrite.IDWriteRenderingParams","dwrite/IDWriteRenderingParams"]
old-location: directwrite\IDWriteRenderingParams.htm
tech.root: DirectWrite
ms.assetid: 28b118e4-9a63-46cf-8ab7-e1039126405b
ms.date: 12/05/2018
ms.keywords: IDWriteRenderingParams, IDWriteRenderingParams interface [Direct Write], IDWriteRenderingParams interface [Direct Write],described, directwrite.IDWriteRenderingParams, dwrite/IDWriteRenderingParams
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteRenderingParams
 - dwrite/IDWriteRenderingParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteRenderingParams
---

# IDWriteRenderingParams interface


## -description

 Represents text rendering settings such as ClearType level, enhanced contrast, and gamma correction for glyph rasterization and filtering.

An application typically obtains a rendering parameters object by calling the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams">IDWriteFactory::CreateMonitorRenderingParams</a> method.

## -inheritance

The <b>IDWriteRenderingParams</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteRenderingParams</b> also has these types of members:

## -see-also

<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams">IDWriteFactory::CreateMonitorRenderingParams</a>

