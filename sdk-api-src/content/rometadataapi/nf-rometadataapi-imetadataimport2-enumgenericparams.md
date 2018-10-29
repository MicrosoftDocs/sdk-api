---
UID: NF:rometadataapi.IMetaDataImport2.EnumGenericParams
title: IMetaDataImport2::EnumGenericParams
author: windows-sdk-content
description: Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.
old-location: winrt\imetadataimport2_enumgenericparams.htm
tech.root: WinRT
ms.assetid: 7ad0d834-7b77-4c90-b28f-fc9e54e9deb7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumGenericParams, EnumGenericParams method [Windows Runtime], EnumGenericParams method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],EnumGenericParams method, IMetaDataImport2.EnumGenericParams, IMetaDataImport2::EnumGenericParams, rometadataapi/IMetaDataImport2::EnumGenericParams, winrt.imetadataimport2_enumgenericparams
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
 - IMetaDataImport2.EnumGenericParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport2::EnumGenericParams


## -description


Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tk [in]

The <b>TypeDef</b> or <b>MethodDef</b> token whose generic parameters are to be enumerated.


### -param rGenericParams [out]

The array of generic parameters to enumerate.


### -param cMax [in]

The requested maximum number of tokens to place in <i>rGenericParams</i>.


### -param pcGenericParams [out]

The returned number of tokens placed in <i>rGenericParams</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumGenericParams</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcGenericParams</i> is set to 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

