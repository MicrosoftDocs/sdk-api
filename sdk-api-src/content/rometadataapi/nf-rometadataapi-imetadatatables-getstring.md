---
UID: NF:rometadataapi.IMetaDataTables.GetString
title: IMetaDataTables::GetString (rometadataapi.h)
description: Gets the string at the specified index from the table column in the current reference scope.
helpviewer_keywords: ["GetString","GetString method [Windows Runtime]","GetString method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetString method","IMetaDataTables.GetString","IMetaDataTables::GetString","rometadataapi/IMetaDataTables::GetString","winrt.imetadatatables_getstring"]
old-location: winrt\imetadatatables_getstring.htm
tech.root: WinRT
ms.assetid: 35b79dac-39c7-4ca2-8608-e7ea64d4574c
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Windows Runtime], GetString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetString method, IMetaDataTables.GetString, IMetaDataTables::GetString, rometadataapi/IMetaDataTables::GetString, winrt.imetadatatables_getstring
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
 - IMetaDataTables::GetString
 - rometadataapi/IMetaDataTables::GetString
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
 - IMetaDataTables.GetString
---

# IMetaDataTables::GetString


## -description

Gets the string at the specified index from the table column in the current reference scope.

## -parameters

### -param ixString [in]

The index at which to start to search for the next value.

### -param ppString [out]

A pointer to a pointer to the returned string value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>