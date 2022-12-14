---
UID: NF:rometadataapi.IMetaDataImport.GetMemberProps
title: IMetaDataImport::GetMemberProps (rometadataapi.h)
description: Gets metadata information, including the name, binary signature, and relative virtual address, of the Type member referenced by the specified metadata token.
helpviewer_keywords: ["GetMemberProps","GetMemberProps method [Windows Runtime]","GetMemberProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetMemberProps method","IMetaDataImport.GetMemberProps","IMetaDataImport::GetMemberProps","rometadataapi/IMetaDataImport::GetMemberProps","winrt.imetadataimport_getmemberprops"]
old-location: winrt\imetadataimport_getmemberprops.htm
tech.root: WinRT
ms.assetid: b278947f-4e84-4438-bb93-11bfd2d56be3
ms.date: 12/05/2018
ms.keywords: GetMemberProps, GetMemberProps method [Windows Runtime], GetMemberProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMemberProps method, IMetaDataImport.GetMemberProps, IMetaDataImport::GetMemberProps, rometadataapi/IMetaDataImport::GetMemberProps, winrt.imetadataimport_getmemberprops
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
 - IMetaDataImport::GetMemberProps
 - rometadataapi/IMetaDataImport::GetMemberProps
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
 - IMetaDataImport.GetMemberProps
---

# IMetaDataImport::GetMemberProps


## -description

Gets metadata information, including the name, binary signature, and relative virtual address, of the Type member referenced by the specified metadata token.

## -parameters

### -param tkMember [in]

The token that references the member to get the associated metadata for.

### -param ptkTypeDef [out]

A pointer to the metadata token that represents the class of the member.

### -param szMember [out]

The name of the member.

### -param cchMember [in]

The size in wide characters of the szMember buffer.

### -param pchMember [out]

The size in wide characters of the returned name.

### -param pdwAttr [out]

Any flag values applied to the member.

### -param ppvSigBlob [out]

A pointer to the binary metadata signature of the member.

### -param pcbSigBlob [out]

The size in bytes of <i>ppvSigBlob</i>.

### -param pulCodeRVA [out]

A pointer to the relative virtual address of the member.

### -param pdwImplFlags [out]

Any method implementation flags associated with the member.

### -param pdwCPlusTypeFlag [out]

A flag that marks a ValueType.

### -param ppValue [out]

A constant string value returned by this member.

### -param pcchValue [out]

The size in characters of <i>ppValue</i>, or zero if <i>ppValue</i> does not hold a string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>