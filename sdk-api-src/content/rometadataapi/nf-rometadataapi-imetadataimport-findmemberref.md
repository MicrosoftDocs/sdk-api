---
UID: NF:rometadataapi.IMetaDataImport.FindMemberRef
title: IMetaDataImport::FindMemberRef (rometadataapi.h)
description: Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified Type and that has the specified name and metadata signature.
helpviewer_keywords: ["FindMemberRef","FindMemberRef method [Windows Runtime]","FindMemberRef method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","FindMemberRef method","IMetaDataImport.FindMemberRef","IMetaDataImport::FindMemberRef","rometadataapi/IMetaDataImport::FindMemberRef","winrt.imetadataimport_findmemberref"]
old-location: winrt\imetadataimport_findmemberref.htm
tech.root: WinRT
ms.assetid: beb32bb3-06e3-4817-90f0-0745756e1955
ms.date: 12/05/2018
ms.keywords: FindMemberRef, FindMemberRef method [Windows Runtime], FindMemberRef method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],FindMemberRef method, IMetaDataImport.FindMemberRef, IMetaDataImport::FindMemberRef, rometadataapi/IMetaDataImport::FindMemberRef, winrt.imetadataimport_findmemberref
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
 - IMetaDataImport::FindMemberRef
 - rometadataapi/IMetaDataImport::FindMemberRef
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
 - IMetaDataImport.FindMemberRef
---

# IMetaDataImport::FindMemberRef


## -description

Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified Type and that has the specified name and metadata signature.

## -parameters

### -param tkTypeRef [in]

The TypeRef token for the class or interface that encloses the member reference to search for. If this value is <b>mdTokenNil</b>, the lookup is done for a global variable or a global-function reference.

### -param szName [in]

The name of the member reference to search for.

### -param pvSigBlob [in]

A pointer to the binary metadata signature of the member reference.

### -param cbSigBlob [in]

The size in bytes of <i>pvSigBlob</i>.

### -param pMemberRef [out]

A pointer to the matching MemberRef token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You specify the member using its enclosing class or interface (<i>tkTypeRef</i>), its name (<i>szName</i>), and optionally its signature (<i>pvSigBlob</i>).

The signature passed to <b>FindMemberRef</b> must have been generated in the current scope, because signatures are bound to a particular scope. A signature can embed a token that identifies the enclosing class or value type. The token is an index into the local TypeDef table. You cannot build a run-time signature outside the context of the current scope and use that signature as input to <b>FindMemberRef</b>.

<b>FindMemberRef</b> finds only member references that were defined directly in the class or interface; it does not find inherited member references.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>