---
UID: NF:rometadataapi.IMetaDataImport2.GetMethodSpecProps
title: IMetaDataImport2::GetMethodSpecProps (rometadataapi.h)
description: Gets the metadata signature of the method referenced by the specified MethodSpec token.
helpviewer_keywords: ["GetMethodSpecProps","GetMethodSpecProps method [Windows Runtime]","GetMethodSpecProps method [Windows Runtime]","IMetaDataImport2 interface","IMetaDataImport2 interface [Windows Runtime]","GetMethodSpecProps method","IMetaDataImport2.GetMethodSpecProps","IMetaDataImport2::GetMethodSpecProps","rometadataapi/IMetaDataImport2::GetMethodSpecProps","winrt.imetadataimport2_getmethodspecprops"]
old-location: winrt\imetadataimport2_getmethodspecprops.htm
tech.root: WinRT
ms.assetid: 498ee212-000d-4204-ae7a-de553bf3ea45
ms.date: 12/05/2018
ms.keywords: GetMethodSpecProps, GetMethodSpecProps method [Windows Runtime], GetMethodSpecProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetMethodSpecProps method, IMetaDataImport2.GetMethodSpecProps, IMetaDataImport2::GetMethodSpecProps, rometadataapi/IMetaDataImport2::GetMethodSpecProps, winrt.imetadataimport2_getmethodspecprops
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
 - IMetaDataImport2::GetMethodSpecProps
 - rometadataapi/IMetaDataImport2::GetMethodSpecProps
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
 - IMetaDataImport2.GetMethodSpecProps
---

# IMetaDataImport2::GetMethodSpecProps


## -description

Gets the metadata signature of the method referenced by the specified MethodSpec token.

## -parameters

### -param mi [in]

A <b>MethodSpec</b> token that represents the instantiation of the method.

### -param tkParent [out]

A pointer to the <b>MethodDef</b> or <b>MethodRef</b> token that represents the method definition.

### -param ppvSigBlob [out]

 A pointer to the binary metadata signature of the method.

### -param pcbSigBlob [out]

The size, in bytes, of <i>ppvSigBlob</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport2">IMetaDataImport2</a>