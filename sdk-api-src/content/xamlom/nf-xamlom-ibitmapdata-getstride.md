---
UID: NF:xamlom.IBitmapData.GetStride
title: IBitmapData::GetStride (xamlom.h)
description: Gets the stride of the data. This is the length in bytes of each row of the bitmap.
helpviewer_keywords: ["GetStride","GetStride method","GetStride method","IBitmapData interface","IBitmapData interface","GetStride method","IBitmapData.GetStride","IBitmapData::GetStride","xaml_diagnostics.ibitmapdata_getstride","xamlom/IBitmapData::GetStride"]
old-location: xaml_diagnostics\ibitmapdata_getstride.htm
tech.root: xaml_diagnostics
ms.assetid: 8D4EAB0A-1976-4A40-932C-AAE67F524B94
ms.date: 12/05/2018
ms.keywords: GetStride, GetStride method, GetStride method,IBitmapData interface, IBitmapData interface,GetStride method, IBitmapData.GetStride, IBitmapData::GetStride, xaml_diagnostics.ibitmapdata_getstride, xamlom/IBitmapData::GetStride
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitmapData::GetStride
 - xamlom/IBitmapData::GetStride
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IBitmapData.GetStride
---

# IBitmapData::GetStride


## -description

Gets the stride of the data. This is the length in bytes of each row of the bitmap.

## -parameters

### -param pStride [out]

The length in bytes of each row of the bitmap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>