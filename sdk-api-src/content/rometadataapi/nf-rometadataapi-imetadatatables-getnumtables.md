---
UID: NF:rometadataapi.IMetaDataTables.GetNumTables
title: IMetaDataTables::GetNumTables (rometadataapi.h)
description: Gets the number of tables in the scope of the current IMetaDataTables instance.
helpviewer_keywords: ["GetNumTables","GetNumTables method [Windows Runtime]","GetNumTables method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetNumTables method","IMetaDataTables.GetNumTables","IMetaDataTables::GetNumTables","rometadataapi/IMetaDataTables::GetNumTables","winrt.imetadatatables_getnumtables"]
old-location: winrt\imetadatatables_getnumtables.htm
tech.root: WinRT
ms.assetid: b5748a90-1ee1-4f76-93c0-2da2fd5d55c1
ms.date: 12/05/2018
ms.keywords: GetNumTables, GetNumTables method [Windows Runtime], GetNumTables method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetNumTables method, IMetaDataTables.GetNumTables, IMetaDataTables::GetNumTables, rometadataapi/IMetaDataTables::GetNumTables, winrt.imetadatatables_getnumtables
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
 - IMetaDataTables::GetNumTables
 - rometadataapi/IMetaDataTables::GetNumTables
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
 - IMetaDataTables.GetNumTables
---

# IMetaDataTables::GetNumTables


## -description

Gets the number of tables in the scope of the current <a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a> instance.

## -parameters

### -param pcTables [out]

A pointer to the number of tables in the current instance scope.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>