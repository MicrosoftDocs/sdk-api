---
UID: NF:rometadataapi.IMetaDataTables.GetBlobHeapSize
title: IMetaDataTables::GetBlobHeapSize (rometadataapi.h)
description: A pointer to a pointer to the binary data retrieved.
helpviewer_keywords: ["GetBlobHeapSize","GetBlobHeapSize method [Windows Runtime]","GetBlobHeapSize method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetBlobHeapSize method","IMetaDataTables.GetBlobHeapSize","IMetaDataTables::GetBlobHeapSize","rometadataapi/IMetaDataTables::GetBlobHeapSize","winrt.imetadatatables_getblobheapsize"]
old-location: winrt\imetadatatables_getblobheapsize.htm
tech.root: WinRT
ms.assetid: 9001b2ee-846e-476b-b1db-7860c25075ee
ms.date: 12/05/2018
ms.keywords: GetBlobHeapSize, GetBlobHeapSize method [Windows Runtime], GetBlobHeapSize method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetBlobHeapSize method, IMetaDataTables.GetBlobHeapSize, IMetaDataTables::GetBlobHeapSize, rometadataapi/IMetaDataTables::GetBlobHeapSize, winrt.imetadatatables_getblobheapsize
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
 - IMetaDataTables::GetBlobHeapSize
 - rometadataapi/IMetaDataTables::GetBlobHeapSize
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
 - IMetaDataTables.GetBlobHeapSize
---

# IMetaDataTables::GetBlobHeapSize


## -description

A pointer to a pointer to the binary data retrieved.

## -parameters

### -param pcbBlobs [out]

A pointer to the size, in bytes, of the BLOB heap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>