---
UID: NF:rometadataapi.IMetaDataImport2.GetGenericParamConstraintProps
title: IMetaDataImport2::GetGenericParamConstraintProps
author: windows-sdk-content
description: Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.
old-location: winrt\imetadataimport2_getgenericparamconstraintprops.htm
old-project: WinRT
ms.assetid: 307b4ab5-733d-4340-a400-3a13039099b0
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetGenericParamConstraintProps, GetGenericParamConstraintProps method [Windows Runtime], GetGenericParamConstraintProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetGenericParamConstraintProps method, IMetaDataImport2.GetGenericParamConstraintProps, IMetaDataImport2::GetGenericParamConstraintProps, rometadataapi/IMetaDataImport2::GetGenericParamConstraintProps, winrt.imetadataimport2_getgenericparamconstraintprops
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport2.GetGenericParamConstraintProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport2::GetGenericParamConstraintProps


## -description


Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.


## -parameters




### -param gpc [in]

The token to the generic parameter constraint for which to return the metadata.


### -param ptGenericParam [out]

A pointer to the token that represents the generic parameter that is constrained.


### -param ptkConstraintType [out]

A pointer to a <b>TypeDef</b>, <b>TypeRef</b>, or <b>TypeSpec</b> token that represents a constraint on ptGenericParam.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

