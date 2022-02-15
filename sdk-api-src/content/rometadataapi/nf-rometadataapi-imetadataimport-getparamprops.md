---
UID: NF:rometadataapi.IMetaDataImport.GetParamProps
title: IMetaDataImport::GetParamProps (rometadataapi.h)
description: Gets metadata values for the parameter referenced by the specified ParamDef token.
helpviewer_keywords: ["GetParamProps","GetParamProps method [Windows Runtime]","GetParamProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetParamProps method","IMetaDataImport.GetParamProps","IMetaDataImport::GetParamProps","rometadataapi/IMetaDataImport::GetParamProps","winrt.imetadataimport_getparamprops"]
old-location: winrt\imetadataimport_getparamprops.htm
tech.root: WinRT
ms.assetid: 76de324f-f371-4fac-ab0a-b7f359dd3abd
ms.date: 12/05/2018
ms.keywords: GetParamProps, GetParamProps method [Windows Runtime], GetParamProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetParamProps method, IMetaDataImport.GetParamProps, IMetaDataImport::GetParamProps, rometadataapi/IMetaDataImport::GetParamProps, winrt.imetadataimport_getparamprops
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
 - IMetaDataImport::GetParamProps
 - rometadataapi/IMetaDataImport::GetParamProps
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
 - IMetaDataImport.GetParamProps
---

# IMetaDataImport::GetParamProps


## -description

Gets metadata values for the parameter referenced by the specified ParamDef token.

## -parameters

### -param tkParamDef [in]

A ParamDef token that represents the parameter to return metadata for.

### -param ptkMethodDef [out]

A pointer to a MethodDef token representing the method that takes the parameter.

### -param pulSequence [out]

The ordinal position of the parameter in the method argument list.

### -param szName [out]

A buffer to hold the name of the parameter.

### -param cchName [in]

The requested size in wide characters of <i>szName</i>.

### -param pchName [out]

The returned size in wide characters of <i>szName</i>.

### -param pdwAttr [out]

A pointer to any attribute flags associated with the parameter.

### -param pdwCPlusTypeFlag [out]

A pointer to a flag specifying that the parameter is a ValueType.

### -param ppValue [out]

A pointer to a constant string returned by the parameter.

### -param pcchValue [out]

The size of <i>ppValue</i> in wide characters, or zero if <i>ppValue</i> does not hold a string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>