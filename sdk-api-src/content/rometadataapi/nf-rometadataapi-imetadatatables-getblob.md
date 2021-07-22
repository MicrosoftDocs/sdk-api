---
UID: NF:rometadataapi.IMetaDataTables.GetBlob
title: IMetaDataTables::GetBlob (rometadataapi.h)
description: Gets a pointer to the binary large object (BLOB) at the specified column index.
helpviewer_keywords: ["GetBlob","GetBlob method [Windows Runtime]","GetBlob method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetBlob method","IMetaDataTables.GetBlob","IMetaDataTables::GetBlob","rometadataapi/IMetaDataTables::GetBlob","winrt.imetadatatables_getblob"]
old-location: winrt\imetadatatables_getblob.htm
tech.root: WinRT
ms.assetid: 1a9da245-a1a9-4004-8925-00b2fe72c9ca
ms.date: 12/05/2018
ms.keywords: GetBlob, GetBlob method [Windows Runtime], GetBlob method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetBlob method, IMetaDataTables.GetBlob, IMetaDataTables::GetBlob, rometadataapi/IMetaDataTables::GetBlob, winrt.imetadatatables_getblob
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
 - IMetaDataTables::GetBlob
 - rometadataapi/IMetaDataTables::GetBlob
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
 - IMetaDataTables.GetBlob
---

# IMetaDataTables::GetBlob


## -description

Gets a pointer to the binary large object (BLOB) at the specified column index.

## -parameters

### -param ixBlob [in]

The memory address from which to get <i>ppData</i>.

### -param pcbData [out]

A pointer to the size, in bytes, of <i>ppData</i>.

### -param ppData [out]

A pointer to a pointer to the binary data retrieved.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>