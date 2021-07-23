---
UID: NF:rometadataapi.IMetaDataTables.GetGuidHeapSize
title: IMetaDataTables::GetGuidHeapSize (rometadataapi.h)
description: Gets the size, in bytes, of the GUID heap.
helpviewer_keywords: ["GetGuidHeapSize","GetGuidHeapSize method [Windows Runtime]","GetGuidHeapSize method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetGuidHeapSize method","IMetaDataTables.GetGuidHeapSize","IMetaDataTables::GetGuidHeapSize","rometadataapi/IMetaDataTables::GetGuidHeapSize","winrt.imetadatatables_getguidheapsize"]
old-location: winrt\imetadatatables_getguidheapsize.htm
tech.root: WinRT
ms.assetid: 56b0f15f-caf3-44e0-8cec-7ca3f2edb74d
ms.date: 12/05/2018
ms.keywords: GetGuidHeapSize, GetGuidHeapSize method [Windows Runtime], GetGuidHeapSize method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetGuidHeapSize method, IMetaDataTables.GetGuidHeapSize, IMetaDataTables::GetGuidHeapSize, rometadataapi/IMetaDataTables::GetGuidHeapSize, winrt.imetadatatables_getguidheapsize
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
 - IMetaDataTables::GetGuidHeapSize
 - rometadataapi/IMetaDataTables::GetGuidHeapSize
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
 - IMetaDataTables.GetGuidHeapSize
---

# IMetaDataTables::GetGuidHeapSize


## -description

Gets the size, in bytes, of the GUID heap.

## -parameters

### -param pcbGuids [out]

A pointer to the size, in bytes, of the GUID heap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>