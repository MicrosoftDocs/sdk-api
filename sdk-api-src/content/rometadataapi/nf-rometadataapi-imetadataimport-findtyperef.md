---
UID: NF:rometadataapi.IMetaDataImport.FindTypeRef
title: IMetaDataImport::FindTypeRef (rometadataapi.h)
description: Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.
helpviewer_keywords: ["FindTypeRef","FindTypeRef method [Windows Runtime]","FindTypeRef method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","FindTypeRef method","IMetaDataImport.FindTypeRef","IMetaDataImport::FindTypeRef","rometadataapi/IMetaDataImport::FindTypeRef","winrt.imetadataimport_findtyperef"]
old-location: winrt\imetadataimport_findtyperef.htm
tech.root: WinRT
ms.assetid: ec89d7c0-b607-4885-b819-3eb8022ad46d
ms.date: 12/05/2018
ms.keywords: FindTypeRef, FindTypeRef method [Windows Runtime], FindTypeRef method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],FindTypeRef method, IMetaDataImport.FindTypeRef, IMetaDataImport::FindTypeRef, rometadataapi/IMetaDataImport::FindTypeRef, winrt.imetadataimport_findtyperef
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
 - IMetaDataImport::FindTypeRef
 - rometadataapi/IMetaDataImport::FindTypeRef
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
 - IMetaDataImport.FindTypeRef
---

# IMetaDataImport::FindTypeRef


## -description

Gets a pointer to the TypeRef token for the Type reference that is in the specified scope and that has the specified name.

## -parameters

### -param tkResolutionScope [in]

A ModuleRef, AssemblyRef, or TypeRef token that specifies the module, assembly, or type, respectively, in which the type reference is defined.

### -param szName [in]

The name of the type reference to search for.

### -param tkTypeRef [out]

A pointer to the matching TypeRef token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>