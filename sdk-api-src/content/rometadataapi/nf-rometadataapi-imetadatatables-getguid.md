---
UID: NF:rometadataapi.IMetaDataTables.GetGuid
title: IMetaDataTables::GetGuid (rometadataapi.h)
description: Gets a GUID from the row at the specified index.
helpviewer_keywords: ["GetGuid","GetGuid method [Windows Runtime]","GetGuid method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetGuid method","IMetaDataTables.GetGuid","IMetaDataTables::GetGuid","rometadataapi/IMetaDataTables::GetGuid","winrt.imetadatatables_getguid"]
old-location: winrt\imetadatatables_getguid.htm
tech.root: WinRT
ms.assetid: 037d722f-3efb-4c01-8445-b23caafbbdb2
ms.date: 12/05/2018
ms.keywords: GetGuid, GetGuid method [Windows Runtime], GetGuid method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetGuid method, IMetaDataTables.GetGuid, IMetaDataTables::GetGuid, rometadataapi/IMetaDataTables::GetGuid, winrt.imetadatatables_getguid
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
 - IMetaDataTables::GetGuid
 - rometadataapi/IMetaDataTables::GetGuid
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
 - IMetaDataTables.GetGuid
---

# IMetaDataTables::GetGuid


## -description

Gets a GUID from the row at the specified index.

## -parameters

### -param ixGuid [in]

The index of the row from which to get the GUID.

### -param ppGUID [out]

A pointer to a pointer to the GUID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We do not recommend the use of this method, because it does not return consistent results. For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics". For more info, see <a href="/dotnet/standard/components#applicable-standards">ECMA C# and Common Language Infrastructure Standards</a> and <a href="https://ecma-international.org/publications-and-standards/standards/ecma-335/">Standard ECMA-335 - Common Language Infrastructure (CLI)</a> on the Ecma International Web site.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>