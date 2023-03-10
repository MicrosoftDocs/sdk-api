---
UID: NF:rometadataapi.IMetaDataTables.GetStringHeapSize
title: IMetaDataTables::GetStringHeapSize (rometadataapi.h)
description: Gets the size, in bytes, of the string heap.
helpviewer_keywords: ["GetStringHeapSize","GetStringHeapSize method [Windows Runtime]","GetStringHeapSize method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetStringHeapSize method","IMetaDataTables.GetStringHeapSize","IMetaDataTables::GetStringHeapSize","rometadataapi/IMetaDataTables::GetStringHeapSize","winrt.imetadatatables_getstringheapsize"]
old-location: winrt\imetadatatables_getstringheapsize.htm
tech.root: WinRT
ms.assetid: 7c830b7c-2651-4efb-9d2d-989b5c25b72e
ms.date: 12/05/2018
ms.keywords: GetStringHeapSize, GetStringHeapSize method [Windows Runtime], GetStringHeapSize method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetStringHeapSize method, IMetaDataTables.GetStringHeapSize, IMetaDataTables::GetStringHeapSize, rometadataapi/IMetaDataTables::GetStringHeapSize, winrt.imetadatatables_getstringheapsize
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataTables::GetStringHeapSize
 - rometadataapi/IMetaDataTables::GetStringHeapSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataTables.GetStringHeapSize
---

# IMetaDataTables::GetStringHeapSize


## -description

Gets the size, in bytes, of the string heap.

## -parameters

### -param pcbStrings [out]

A pointer to the size, in bytes, of the string heap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>