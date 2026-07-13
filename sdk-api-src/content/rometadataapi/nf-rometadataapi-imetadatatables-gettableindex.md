---
UID: NF:rometadataapi.IMetaDataTables.GetTableIndex
title: IMetaDataTables::GetTableIndex (rometadataapi.h)
description: Gets the index for the table referenced by the specified token.
helpviewer_keywords: ["GetTableIndex","GetTableIndex method [Windows Runtime]","GetTableIndex method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetTableIndex method","IMetaDataTables.GetTableIndex","IMetaDataTables::GetTableIndex","rometadataapi/IMetaDataTables::GetTableIndex","winrt.imetadatatables_gettableindex"]
old-location: winrt\imetadatatables_gettableindex.htm
tech.root: WinRT
ms.assetid: 4bc00076-f706-4941-84bd-f1b9c61934e5
ms.date: 12/05/2018
ms.keywords: GetTableIndex, GetTableIndex method [Windows Runtime], GetTableIndex method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetTableIndex method, IMetaDataTables.GetTableIndex, IMetaDataTables::GetTableIndex, rometadataapi/IMetaDataTables::GetTableIndex, winrt.imetadatatables_gettableindex
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
 - IMetaDataTables::GetTableIndex
 - rometadataapi/IMetaDataTables::GetTableIndex
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
 - IMetaDataTables.GetTableIndex
---

# IMetaDataTables::GetTableIndex


## -description

Gets the index for the table referenced by the specified token.

## -parameters

### -param token [in]

The token that references the table.

### -param pixTbl [out]

A pointer to the returned index for the referenced table.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". For more info, see <a href="/dotnet/standard/components#applicable-standards">ECMA C# and Common Language Infrastructure Standards</a> and <a href="https://ecma-international.org/publications-and-standards/standards/ecma-335/">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>