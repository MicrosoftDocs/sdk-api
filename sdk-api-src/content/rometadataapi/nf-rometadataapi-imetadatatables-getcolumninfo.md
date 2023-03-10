---
UID: NF:rometadataapi.IMetaDataTables.GetColumnInfo
title: IMetaDataTables::GetColumnInfo (rometadataapi.h)
description: Gets data about the specified column in the specified table.
helpviewer_keywords: ["GetColumnInfo","GetColumnInfo method [Windows Runtime]","GetColumnInfo method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetColumnInfo method","IMetaDataTables.GetColumnInfo","IMetaDataTables::GetColumnInfo","rometadataapi/IMetaDataTables::GetColumnInfo","winrt.imetadatatables_getcolumninfo"]
old-location: winrt\imetadatatables_getcolumninfo.htm
tech.root: WinRT
ms.assetid: aea7944a-87db-496c-869d-e9e2fa87e9af
ms.date: 12/05/2018
ms.keywords: GetColumnInfo, GetColumnInfo method [Windows Runtime], GetColumnInfo method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetColumnInfo method, IMetaDataTables.GetColumnInfo, IMetaDataTables::GetColumnInfo, rometadataapi/IMetaDataTables::GetColumnInfo, winrt.imetadatatables_getcolumninfo
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
 - IMetaDataTables::GetColumnInfo
 - rometadataapi/IMetaDataTables::GetColumnInfo
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
 - IMetaDataTables.GetColumnInfo
---

# IMetaDataTables::GetColumnInfo


## -description

Gets data about the specified column in the specified table.

## -parameters

### -param ixTbl [in]

The index of the desired table.

### -param ixCol [in]

The index of the desired column.

### -param poCol [out]

A pointer to the offset of the column in the row.

### -param pcbCol [out]

 A pointer to the size, in bytes, of the column.

### -param pType [out]

A pointer to the type of the values in the column.

### -param ppName [out]

A pointer to a pointer to the column name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>