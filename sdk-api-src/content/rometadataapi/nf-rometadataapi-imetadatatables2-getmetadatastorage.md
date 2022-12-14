---
UID: NF:rometadataapi.IMetaDataTables2.GetMetaDataStorage
title: IMetaDataTables2::GetMetaDataStorage (rometadataapi.h)
description: Gets the size and contents of the metadata stored in the specified section.
helpviewer_keywords: ["GetMetaDataStorage","GetMetaDataStorage method [Windows Runtime]","GetMetaDataStorage method [Windows Runtime]","IMetaDataTables2 interface","IMetaDataTables2 interface [Windows Runtime]","GetMetaDataStorage method","IMetaDataTables2.GetMetaDataStorage","IMetaDataTables2::GetMetaDataStorage","rometadataapi/IMetaDataTables2::GetMetaDataStorage","winrt.imetadatatables2_getmetadatastorage"]
old-location: winrt\imetadatatables2_getmetadatastorage.htm
tech.root: WinRT
ms.assetid: 7de4fccb-9cd6-443d-bbd3-ba545e040ca6
ms.date: 12/05/2018
ms.keywords: GetMetaDataStorage, GetMetaDataStorage method [Windows Runtime], GetMetaDataStorage method [Windows Runtime],IMetaDataTables2 interface, IMetaDataTables2 interface [Windows Runtime],GetMetaDataStorage method, IMetaDataTables2.GetMetaDataStorage, IMetaDataTables2::GetMetaDataStorage, rometadataapi/IMetaDataTables2::GetMetaDataStorage, winrt.imetadatatables2_getmetadatastorage
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
 - IMetaDataTables2::GetMetaDataStorage
 - rometadataapi/IMetaDataTables2::GetMetaDataStorage
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
 - IMetaDataTables2.GetMetaDataStorage
---

# IMetaDataTables2::GetMetaDataStorage


## -description

Gets the size and contents of the metadata stored in the specified section.

## -parameters

### -param ppvMd [out]

A pointer to a metadata section.

### -param pcbMd [out]

The size of the metadata stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables2">IMetaDataTables2</a>