---
UID: NF:rometadataapi.IMetaDataTables.GetUserString
title: IMetaDataTables::GetUserString (rometadataapi.h)
description: Gets the hard-coded string at the specified index in the string column in the current scope.
helpviewer_keywords: ["GetUserString","GetUserString method [Windows Runtime]","GetUserString method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetUserString method","IMetaDataTables.GetUserString","IMetaDataTables::GetUserString","rometadataapi/IMetaDataTables::GetUserString","winrt.imetadatatables_getuserstring"]
old-location: winrt\imetadatatables_getuserstring.htm
tech.root: WinRT
ms.assetid: 868f6be3-1baf-4f7c-be10-12b79a45e9c7
ms.date: 12/05/2018
ms.keywords: GetUserString, GetUserString method [Windows Runtime], GetUserString method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetUserString method, IMetaDataTables.GetUserString, IMetaDataTables::GetUserString, rometadataapi/IMetaDataTables::GetUserString, winrt.imetadatatables_getuserstring
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
 - IMetaDataTables::GetUserString
 - rometadataapi/IMetaDataTables::GetUserString
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
 - IMetaDataTables.GetUserString
---

# IMetaDataTables::GetUserString


## -description

Gets the hard-coded string at the specified index in the string column in the current scope.

## -parameters

### -param ixUserString [in]

The index value from which the hard-coded string will be retrieved.

### -param pcbData [out]

A pointer to the size of <i>ppData</i>.

### -param ppData [out]

A pointer to a pointer to the returned string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>