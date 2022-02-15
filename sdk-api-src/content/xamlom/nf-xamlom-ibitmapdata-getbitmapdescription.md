---
UID: NF:xamlom.IBitmapData.GetBitmapDescription
title: IBitmapData::GetBitmapDescription (xamlom.h)
description: Gets a BitmapDescription that describes the bitmap data stored in the IBitmapData.
helpviewer_keywords: ["GetBitmapDescription","GetBitmapDescription method","GetBitmapDescription method","IBitmapData interface","IBitmapData interface","GetBitmapDescription method","IBitmapData.GetBitmapDescription","IBitmapData::GetBitmapDescription","xaml_diagnostics.ibitmapdata_getbitmapdescription","xamlom/IBitmapData::GetBitmapDescription"]
old-location: xaml_diagnostics\ibitmapdata_getbitmapdescription.htm
tech.root: xaml_diagnostics
ms.assetid: B10BF4E3-C9C2-41E6-99FC-671F6BE47278
ms.date: 12/05/2018
ms.keywords: GetBitmapDescription, GetBitmapDescription method, GetBitmapDescription method,IBitmapData interface, IBitmapData interface,GetBitmapDescription method, IBitmapData.GetBitmapDescription, IBitmapData::GetBitmapDescription, xaml_diagnostics.ibitmapdata_getbitmapdescription, xamlom/IBitmapData::GetBitmapDescription
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
 - IBitmapData::GetBitmapDescription
 - xamlom/IBitmapData::GetBitmapDescription
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
 - IBitmapData.GetBitmapDescription
---

# IBitmapData::GetBitmapDescription


## -description

Gets a <a href="/previous-versions/windows/desktop/api/xamlom/ns-xamlom-bitmapdescription">BitmapDescription</a> that describes the bitmap data stored in the <a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>.

## -parameters

### -param pBitmapDescription [out]

Information about the bitmap stored in the <a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>