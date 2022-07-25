---
UID: NF:rometadataapi.IMetaDataTables2.GetMetaDataStreamInfo
title: IMetaDataTables2::GetMetaDataStreamInfo (rometadataapi.h)
description: Gets the name, size, and contents of the metadata stream at the specified index.
helpviewer_keywords: ["GetMetaDataStreamInfo","GetMetaDataStreamInfo method [Windows Runtime]","GetMetaDataStreamInfo method [Windows Runtime]","IMetaDataTables2 interface","IMetaDataTables2 interface [Windows Runtime]","GetMetaDataStreamInfo method","IMetaDataTables2.GetMetaDataStreamInfo","IMetaDataTables2::GetMetaDataStreamInfo","rometadataapi/IMetaDataTables2::GetMetaDataStreamInfo","winrt.imetadatatables2_getmetadatastreaminfo"]
old-location: winrt\imetadatatables2_getmetadatastreaminfo.htm
tech.root: WinRT
ms.assetid: a292a32a-b9c2-46b5-a2c4-074e616d7675
ms.date: 12/05/2018
ms.keywords: GetMetaDataStreamInfo, GetMetaDataStreamInfo method [Windows Runtime], GetMetaDataStreamInfo method [Windows Runtime],IMetaDataTables2 interface, IMetaDataTables2 interface [Windows Runtime],GetMetaDataStreamInfo method, IMetaDataTables2.GetMetaDataStreamInfo, IMetaDataTables2::GetMetaDataStreamInfo, rometadataapi/IMetaDataTables2::GetMetaDataStreamInfo, winrt.imetadatatables2_getmetadatastreaminfo
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
 - IMetaDataTables2::GetMetaDataStreamInfo
 - rometadataapi/IMetaDataTables2::GetMetaDataStreamInfo
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
 - IMetaDataTables2.GetMetaDataStreamInfo
---

# IMetaDataTables2::GetMetaDataStreamInfo


## -description

Gets the name, size, and contents of the metadata stream at the specified index.

## -parameters

### -param ix [in]

The index of the requested metadata stream.

### -param ppchName [out]

A pointer to the name of the stream.

### -param ppv [out]

 A pointer to the metadata stream.

### -param pcb [out]

The size, in bytes, of <i>ppv</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables2">IMetaDataTables2</a>