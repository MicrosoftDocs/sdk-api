---
UID: NF:rometadataapi.IMetaDataImport.GetMemberRefProps
title: IMetaDataImport::GetMemberRefProps (rometadataapi.h)
description: Gets metadata associated with the member referenced by the specified token.
helpviewer_keywords: ["GetMemberRefProps","GetMemberRefProps method [Windows Runtime]","GetMemberRefProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetMemberRefProps method","IMetaDataImport.GetMemberRefProps","IMetaDataImport::GetMemberRefProps","rometadataapi/IMetaDataImport::GetMemberRefProps","winrt.imetadataimport_getmemberrefprops"]
old-location: winrt\imetadataimport_getmemberrefprops.htm
tech.root: WinRT
ms.assetid: a82baa9a-0102-4d30-945d-34ec2514e0a6
ms.date: 12/05/2018
ms.keywords: GetMemberRefProps, GetMemberRefProps method [Windows Runtime], GetMemberRefProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMemberRefProps method, IMetaDataImport.GetMemberRefProps, IMetaDataImport::GetMemberRefProps, rometadataapi/IMetaDataImport::GetMemberRefProps, winrt.imetadataimport_getmemberrefprops
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
 - IMetaDataImport::GetMemberRefProps
 - rometadataapi/IMetaDataImport::GetMemberRefProps
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
 - IMetaDataImport.GetMemberRefProps
---

# IMetaDataImport::GetMemberRefProps


## -description

Gets metadata associated with the member referenced by the specified token.

## -parameters

### -param tkMemberRef [in]

The MemberRef token to return associated metadata for.

### -param ptk [out]

A TypeDef or TypeRef, or TypeSpec token that represents the class that declares the member, or a ModuleRef token that represents the module class that declares the member, or a MethodDef that represents the member.

### -param szMember [out]

A string buffer for the member's name.

### -param cchMember [in]

The requested size in wide characters of <i>szMember</i>.

### -param pchMember [out]

The returned size in wide characters of <i>szMember</i>.

### -param ppvSigBlob [out]

A pointer to the binary metadata signature for the member.

### -param pcbSigBlob [out]

The size in bytes of <i>ppvSigBlob</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>