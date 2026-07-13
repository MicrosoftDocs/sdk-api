---
UID: NF:rometadataapi.IMetaDataTables.GetUserStringHeapSize
title: IMetaDataTables::GetUserStringHeapSize (rometadataapi.h)
description: Gets the size, in bytes, of the user string heap.
helpviewer_keywords: ["GetUserStringHeapSize","GetUserStringHeapSize method [Windows Runtime]","GetUserStringHeapSize method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetUserStringHeapSize method","IMetaDataTables.GetUserStringHeapSize","IMetaDataTables::GetUserStringHeapSize","rometadataapi/IMetaDataTables::GetUserStringHeapSize","winrt.imetadatatables_getuserstringheapsize"]
old-location: winrt\imetadatatables_getuserstringheapsize.htm
tech.root: WinRT
ms.assetid: f01059be-6370-4bab-b4f4-69db158c17a3
ms.date: 12/05/2018
ms.keywords: GetUserStringHeapSize, GetUserStringHeapSize method [Windows Runtime], GetUserStringHeapSize method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetUserStringHeapSize method, IMetaDataTables.GetUserStringHeapSize, IMetaDataTables::GetUserStringHeapSize, rometadataapi/IMetaDataTables::GetUserStringHeapSize, winrt.imetadatatables_getuserstringheapsize
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
 - IMetaDataTables::GetUserStringHeapSize
 - rometadataapi/IMetaDataTables::GetUserStringHeapSize
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
 - IMetaDataTables.GetUserStringHeapSize
---

# IMetaDataTables::GetUserStringHeapSize


## -description

Gets the size, in bytes, of the user string heap.

## -parameters

### -param pcbUserStrings [out]

A pointer to the size, in bytes, of the user string heap.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>