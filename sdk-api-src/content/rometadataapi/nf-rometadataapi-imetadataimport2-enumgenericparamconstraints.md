---
UID: NF:rometadataapi.IMetaDataImport2.EnumGenericParamConstraints
title: IMetaDataImport2::EnumGenericParamConstraints
author: windows-sdk-content
description: Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.
old-location: winrt\imetadataimport2_enumgenericparamconstraints.htm
tech.root: WinRT
ms.assetid: 5e8ba48d-7c94-4fc6-8def-db296065fdce
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumGenericParamConstraints, EnumGenericParamConstraints method [Windows Runtime], EnumGenericParamConstraints method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],EnumGenericParamConstraints method, IMetaDataImport2.EnumGenericParamConstraints, IMetaDataImport2::EnumGenericParamConstraints, rometadataapi/IMetaDataImport2::EnumGenericParamConstraints, winrt.imetadataimport2_enumgenericparamconstraints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport2.EnumGenericParamConstraints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rometadataapi.h
: 
- IMetaDataImport2.EnumGenericParamConstraints
: 
---

# IMetaDataImport2::EnumGenericParamConstraints


## -description


Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tk [in]

A token that represents the generic parameter whose constraints are to be enumerated.


### -param rGenericParamConstraints [out]

The array of generic parameter constraints to enumerate.


### -param cMax [in]

The requested maximum number of tokens to place in <i>rGenericParamConstraints</i>.


### -param pcGenericParamConstraints [out]

A pointer to the number of tokens placed in <i>rGenericParamConstraints</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumGenericParamConstraints</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcGenericParameterConstraints</i> is set to 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

