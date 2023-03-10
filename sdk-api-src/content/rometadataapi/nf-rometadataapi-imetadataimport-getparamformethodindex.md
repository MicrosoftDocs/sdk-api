---
UID: NF:rometadataapi.IMetaDataImport.GetParamForMethodIndex
title: IMetaDataImport::GetParamForMethodIndex (rometadataapi.h)
description: Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.
helpviewer_keywords: ["GetParamForMethodIndex","GetParamForMethodIndex method [Windows Runtime]","GetParamForMethodIndex method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetParamForMethodIndex method","IMetaDataImport.GetParamForMethodIndex","IMetaDataImport::GetParamForMethodIndex","rometadataapi/IMetaDataImport::GetParamForMethodIndex","winrt.imetadataimport_getparamformethodindex"]
old-location: winrt\imetadataimport_getparamformethodindex.htm
tech.root: WinRT
ms.assetid: 118a5ab3-b7db-4e0c-bf45-ab7e2e0e4f03
ms.date: 12/05/2018
ms.keywords: GetParamForMethodIndex, GetParamForMethodIndex method [Windows Runtime], GetParamForMethodIndex method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetParamForMethodIndex method, IMetaDataImport.GetParamForMethodIndex, IMetaDataImport::GetParamForMethodIndex, rometadataapi/IMetaDataImport::GetParamForMethodIndex, winrt.imetadataimport_getparamformethodindex
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
 - IMetaDataImport::GetParamForMethodIndex
 - rometadataapi/IMetaDataImport::GetParamForMethodIndex
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
 - IMetaDataImport.GetParamForMethodIndex
---

# IMetaDataImport::GetParamForMethodIndex


## -description

Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.

## -parameters

### -param tkMethodDef [in]

A token that represents the method to return the parameter token for.

### -param ulParamSeq [in]

The ordinal position in the parameter list where the requested parameter occurs. Parameters are numbered starting from one, with the method's return value in position zero.

### -param ptkParamDef [out]

A pointer to a ParamDef token that represents the requested parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>