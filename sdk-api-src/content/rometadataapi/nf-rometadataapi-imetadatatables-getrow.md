---
UID: NF:rometadataapi.IMetaDataTables.GetRow
title: IMetaDataTables::GetRow (rometadataapi.h)
description: Gets the row at the specified row index, in the table at the specified table index.
helpviewer_keywords: ["GetRow","GetRow method [Windows Runtime]","GetRow method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetRow method","IMetaDataTables.GetRow","IMetaDataTables::GetRow","rometadataapi/IMetaDataTables::GetRow","winrt.imetadatatables_getrow"]
old-location: winrt\imetadatatables_getrow.htm
tech.root: WinRT
ms.assetid: d56bc0c8-0a63-48c8-bc2c-e3b4c2f313b8
ms.date: 12/05/2018
ms.keywords: GetRow, GetRow method [Windows Runtime], GetRow method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetRow method, IMetaDataTables.GetRow, IMetaDataTables::GetRow, rometadataapi/IMetaDataTables::GetRow, winrt.imetadatatables_getrow
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
 - IMetaDataTables::GetRow
 - rometadataapi/IMetaDataTables::GetRow
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
 - IMetaDataTables.GetRow
---

# IMetaDataTables::GetRow


## -description

Gets the row at the specified row index, in the table at the specified table index.

## -parameters

### -param ixTbl [in]

The index of the table from which the row will be retrieved.

### -param rid [in]

The index of the row to get.

### -param ppRow [out]

A pointer to a pointer to the row.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". The documentation is available online; see <a href="/dotnet/standard/components#applicable-standards">ECMA C# and Common Language Infrastructure Standards</a> on MSDN and <a href="https://www.ecma-international.org/publications/standards/Ecma-335.htm">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>