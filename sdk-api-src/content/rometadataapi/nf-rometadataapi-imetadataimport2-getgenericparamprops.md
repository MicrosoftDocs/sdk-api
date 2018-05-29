---
UID: NF:rometadataapi.IMetaDataImport2.GetGenericParamProps
title: IMetaDataImport2::GetGenericParamProps
author: windows-sdk-content
description: Gets the metadata associated with the generic parameter represented by the specified token.
old-location: winrt\imetadataimport2_getgenericparamprops.htm
old-project: WinRT
ms.assetid: 3967e82c-64e3-4d05-b10a-e4e86f9f60ab
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: GetGenericParamProps, GetGenericParamProps method [Windows Runtime], GetGenericParamProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetGenericParamProps method, IMetaDataImport2.GetGenericParamProps, IMetaDataImport2::GetGenericParamProps, rometadataapi/IMetaDataImport2::GetGenericParamProps, winrt.imetadataimport2_getgenericparamprops
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
-	IMetaDataImport2.GetGenericParamProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport2::GetGenericParamProps


## -description


Gets the metadata associated with the generic parameter represented by the specified token.


## -parameters




### -param gp [in]

The token that represents the generic parameter for which to return metadata.


### -param pulParamSeq [out]

The ordinal position of the Type parameter in the parent constructor or method.


### -param pdwParamFlags [out]

 A value of the <a href="http://msdn.microsoft.com/en-us/library/ms230535.aspx">CorGenericParamAttr</a> enumeration that describes the Type for the generic parameter.


### -param ptOwner [out]

A  <b>TypeDef</b> or <b>MethodDef</b> token that represents the owner of the parameter.


### -param reserved [out]

Reserved for future extensibility.


### -param wzname [out]

The name of the generic parameter.


### -param cchName [in]

The size of the <i>wzName</i> buffer.


### -param pchName [out]

The returned size of the name, in wide characters.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

