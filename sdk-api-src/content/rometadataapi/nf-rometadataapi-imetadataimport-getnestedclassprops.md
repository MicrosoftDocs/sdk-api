---
UID: NF:rometadataapi.IMetaDataImport.GetNestedClassProps
title: IMetaDataImport::GetNestedClassProps (rometadataapi.h)
description: Gets the TypeDef token for the parent Type of the specified nested type.
helpviewer_keywords: ["GetNestedClassProps","GetNestedClassProps method [Windows Runtime]","GetNestedClassProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetNestedClassProps method","IMetaDataImport.GetNestedClassProps","IMetaDataImport::GetNestedClassProps","rometadataapi/IMetaDataImport::GetNestedClassProps","winrt.imetadataimport_getnestedclassprops"]
old-location: winrt\imetadataimport_getnestedclassprops.htm
tech.root: WinRT
ms.assetid: 5633d226-8f02-4527-b435-b75b1e1d5064
ms.date: 12/05/2018
ms.keywords: GetNestedClassProps, GetNestedClassProps method [Windows Runtime], GetNestedClassProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetNestedClassProps method, IMetaDataImport.GetNestedClassProps, IMetaDataImport::GetNestedClassProps, rometadataapi/IMetaDataImport::GetNestedClassProps, winrt.imetadataimport_getnestedclassprops
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
 - IMetaDataImport::GetNestedClassProps
 - rometadataapi/IMetaDataImport::GetNestedClassProps
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
 - IMetaDataImport.GetNestedClassProps
---

# IMetaDataImport::GetNestedClassProps


## -description

Gets the TypeDef token for the parent Type of the specified nested type.

## -parameters

### -param tdNestedClass [in]

A TypeDef token representing the Type to return the parent class token for.

### -param ptdEnclosingClass [out]

A pointer to the TypeDef token for the Type that <i>tdNestedClass</i> is nested in.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>