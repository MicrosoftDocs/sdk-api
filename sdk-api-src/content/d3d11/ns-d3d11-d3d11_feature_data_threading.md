---
UID: NS:d3d11.D3D11_FEATURE_DATA_THREADING
title: D3D11_FEATURE_DATA_THREADING (d3d11.h)
description: Describes the multi-threading features that are supported by the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_THREADING","D3D11_FEATURE_DATA_THREADING structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_THREADING","direct3d11.d3d11_feature_data_threading","ef972430-170a-436c-cbf4-65409cc60040"]
old-location: direct3d11\d3d11_feature_data_threading.htm
tech.root: direct3d11
ms.assetid: 1ad7d4c4-9da2-42b0-a461-e514060e3005
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_THREADING, D3D11_FEATURE_DATA_THREADING structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_THREADING, direct3d11.d3d11_feature_data_threading, ef972430-170a-436c-cbf4-65409cc60040
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_THREADING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_THREADING
 - d3d11/D3D11_FEATURE_DATA_THREADING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_THREADING
---

# D3D11_FEATURE_DATA_THREADING structure


## -description

Describes the multi-threading features that are supported by the current graphics driver.

## -struct-fields

### -field DriverConcurrentCreates

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> means resources can be created concurrently on multiple threads while drawing; <b>FALSE</b> means that the presence of coarse synchronization will prevent concurrency.

### -field DriverCommandLists

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> means command lists are supported by the current driver; <b>FALSE</b> means that the API will emulate deferred contexts and command lists with software.

## -remarks

Use the D3D11_FEATURE_DATA_THREADING structure with the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> method to determine multi-threading support.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>