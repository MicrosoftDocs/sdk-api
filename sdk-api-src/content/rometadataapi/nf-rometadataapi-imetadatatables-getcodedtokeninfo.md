---
UID: NF:rometadataapi.IMetaDataTables.GetCodedTokenInfo
title: IMetaDataTables::GetCodedTokenInfo (rometadataapi.h)
description: Gets a pointer to an array of tokens associated with the specified row index.
helpviewer_keywords: ["GetCodedTokenInfo","GetCodedTokenInfo method [Windows Runtime]","GetCodedTokenInfo method [Windows Runtime]","IMetaDataTables interface","IMetaDataTables interface [Windows Runtime]","GetCodedTokenInfo method","IMetaDataTables.GetCodedTokenInfo","IMetaDataTables::GetCodedTokenInfo","rometadataapi/IMetaDataTables::GetCodedTokenInfo","winrt.imetadatatables_getcodedtokeninfo"]
old-location: winrt\imetadatatables_getcodedtokeninfo.htm
tech.root: WinRT
ms.assetid: 6467affc-0f86-4926-b72f-629c6580e1bf
ms.date: 12/05/2018
ms.keywords: GetCodedTokenInfo, GetCodedTokenInfo method [Windows Runtime], GetCodedTokenInfo method [Windows Runtime],IMetaDataTables interface, IMetaDataTables interface [Windows Runtime],GetCodedTokenInfo method, IMetaDataTables.GetCodedTokenInfo, IMetaDataTables::GetCodedTokenInfo, rometadataapi/IMetaDataTables::GetCodedTokenInfo, winrt.imetadatatables_getcodedtokeninfo
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
 - IMetaDataTables::GetCodedTokenInfo
 - rometadataapi/IMetaDataTables::GetCodedTokenInfo
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
 - IMetaDataTables.GetCodedTokenInfo
---

# IMetaDataTables::GetCodedTokenInfo


## -description

Gets a pointer to an array of tokens associated with the specified row index.

## -parameters

### -param ixCdTkn [in]

The kind of coded token to return.

### -param pcTokens [out]

A pointer to the length of <i>ppTokens</i>.

### -param ppTokens [out]

A pointer to a pointer to an array that contains the list of returned tokens.

### -param ppName [out]

A pointer to a pointer to the name of the token at <i>ixCdTkn</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatatables">IMetaDataTables</a>