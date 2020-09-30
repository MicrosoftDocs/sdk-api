---
UID: NF:rometadataapi.IMetaDataImport.EnumParams
title: IMetaDataImport::EnumParams (rometadataapi.h)
description: Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.
helpviewer_keywords: ["EnumParams","EnumParams method [Windows Runtime]","EnumParams method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumParams method","IMetaDataImport.EnumParams","IMetaDataImport::EnumParams","rometadataapi/IMetaDataImport::EnumParams","winrt.imetadataimport_enumparams"]
old-location: winrt\imetadataimport_enumparams.htm
tech.root: WinRT
ms.assetid: 0d3cc66e-575d-4451-bab7-e3dd24fd5060
ms.date: 12/05/2018
ms.keywords: EnumParams, EnumParams method [Windows Runtime], EnumParams method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumParams method, IMetaDataImport.EnumParams, IMetaDataImport::EnumParams, rometadataapi/IMetaDataImport::EnumParams, winrt.imetadataimport_enumparams
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
 - IMetaDataImport::EnumParams
 - rometadataapi/IMetaDataImport::EnumParams
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
 - IMetaDataImport.EnumParams
---

# IMetaDataImport::EnumParams


## -description

Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.

## -parameters

### -param phEnum [in, out]

 A pointer to the enumerator. This must be NULL for the first call of this method.

### -param tkMethodDef [in]

A MethodDef token representing the method with the parameters to enumerate.

### -param rParams [out]

The array used to store the ParamDef tokens.

### -param cMax [in]

The maximum size of the <i>rParams array</i>.

### -param pcTokens [out]

The number of ParamDef tokens returned in <i>rParams</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumParams</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>