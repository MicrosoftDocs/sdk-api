---
UID: NF:rometadataapi.IMetaDataImport.GetMethodProps
title: IMetaDataImport::GetMethodProps (rometadataapi.h)
description: Gets the metadata associated with the method referenced by the specified MethodDef token.
helpviewer_keywords: ["GetMethodProps","GetMethodProps method [Windows Runtime]","GetMethodProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetMethodProps method","IMetaDataImport.GetMethodProps","IMetaDataImport::GetMethodProps","rometadataapi/IMetaDataImport::GetMethodProps","winrt.imetadataimport_getmethodprops"]
old-location: winrt\imetadataimport_getmethodprops.htm
tech.root: WinRT
ms.assetid: 973f2a8c-025d-4d27-ac99-56902b1132dd
ms.date: 12/05/2018
ms.keywords: GetMethodProps, GetMethodProps method [Windows Runtime], GetMethodProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMethodProps method, IMetaDataImport.GetMethodProps, IMetaDataImport::GetMethodProps, rometadataapi/IMetaDataImport::GetMethodProps, winrt.imetadataimport_getmethodprops
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
 - IMetaDataImport::GetMethodProps
 - rometadataapi/IMetaDataImport::GetMethodProps
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
 - IMetaDataImport.GetMethodProps
---

# IMetaDataImport::GetMethodProps


## -description

Gets the metadata associated with the method referenced by the specified MethodDef token.

## -parameters

### -param tkMethodDef [in]

The MethodDef token that represents the method to return metadata for.

### -param ptkClass [out]

A Pointer to a TypeDef token that represents the type that implements the method.

### -param szMethod [out]

A Pointer to a buffer that has the method's name.

### -param cchMethod [in]

The requested size of <i>szMethod</i>.

### -param pchMethod [out]

A pointer to the size in wide characters of <i>szMethod</i>, or in the case of truncation, the actual number of wide characters in the method name.

### -param pdwAttr [out]

A pointer to any flags associated with the method.

### -param ppvSigBlob [out]

A pointer to the binary metadata signature of the method.

### -param pcbSigBlob [out]

A pointer to the size in bytes of <i>ppvSigBlob</i>.

### -param pulCodeRVA [out]

A pointer to the relative virtual address of the method.

### -param pdwImplFlags [out]

A pointer to any implementation flags for the method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>