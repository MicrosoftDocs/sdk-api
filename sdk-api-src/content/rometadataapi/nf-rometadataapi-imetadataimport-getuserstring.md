---
UID: NF:rometadataapi.IMetaDataImport.GetUserString
title: IMetaDataImport::GetUserString (rometadataapi.h)
description: Gets the literal string represented by the specified metadata token.
helpviewer_keywords: ["GetUserString","GetUserString method [Windows Runtime]","GetUserString method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetUserString method","IMetaDataImport.GetUserString","IMetaDataImport::GetUserString","rometadataapi/IMetaDataImport::GetUserString","winrt.imetadataimport_getuserstring"]
old-location: winrt\imetadataimport_getuserstring.htm
tech.root: WinRT
ms.assetid: c809d878-7c9a-4759-83c8-31cb0a72ee9d
ms.date: 12/05/2018
ms.keywords: GetUserString, GetUserString method [Windows Runtime], GetUserString method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetUserString method, IMetaDataImport.GetUserString, IMetaDataImport::GetUserString, rometadataapi/IMetaDataImport::GetUserString, winrt.imetadataimport_getuserstring
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
 - IMetaDataImport::GetUserString
 - rometadataapi/IMetaDataImport::GetUserString
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
 - IMetaDataImport.GetUserString
---

# IMetaDataImport::GetUserString


## -description

Gets the literal string represented by the specified metadata token.

## -parameters

### -param tkString [in]

The String token to return the associated string for.

### -param szString [out]

A copy of the requested string.

### -param cchString [in]

The maximum size in wide characters of the requested <i>szString</i>.

### -param pchString [out]

The size in wide characters of the returned <i>szString</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>