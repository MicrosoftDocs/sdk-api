---
UID: NF:rometadataapi.IMetaDataTables.GetNextGuid
title: IMetaDataTables::GetNextGuid (rometadataapi.h)
description: Gets the index of the next GUID value in the current table column.
helpviewer_keywords: ["GetNextGuid","GetNextGuid method [Windows Runtime]","GetNextGuid method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetNextGuid method","IMetaDataTables.GetNextGuid","IMetaDataTables::GetNextGuid","rometadataapi/IMetaDataTables::GetNextGuid","winrt.imetadatatables_getnextguid"]
old-location: winrt\imetadatatables_getnextguid.htm
tech.root: WinRT
ms.assetid: b624f727-8371-49a1-8ec7-7110d9b8f971
ms.date: 12/05/2018
ms.keywords: GetNextGuid, GetNextGuid method [Windows Runtime], GetNextGuid method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNextGuid method, IMetaDataTables.GetNextGuid, IMetaDataTables::GetNextGuid, rometadataapi/IMetaDataTables::GetNextGuid, winrt.imetadatatables_getnextguid
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
 - IMetaDataTables::GetNextGuid
 - rometadataapi/IMetaDataTables::GetNextGuid
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
 - IMetaDataTables.GetNextGuid
---

# IMetaDataTables::GetNextGuid


## -description

Gets the index of the next GUID value in the current table column.

## -parameters

### -param ixGuid [in]

The index value from a GUID table column.

### -param pNext [out]

A pointer to the index of the next GUID value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". For more info, see <a href="/dotnet/standard/components#applicable-standards">ECMA C# and Common Language Infrastructure Standards</a> and <a href="https://ecma-international.org/publications-and-standards/standards/ecma-335/">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>