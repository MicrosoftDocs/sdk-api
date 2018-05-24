---
UID: NF:rometadataapi.IMetaDataImport.GetCustomAttributeProps
title: IMetaDataImport::GetCustomAttributeProps
author: windows-driver-content
description: Gets the value of the custom attribute, given its metadata token.
old-location: winrt\imetadataimport_getcustomattributeprops.htm
old-project: WinRT
ms.assetid: ccb8891c-ceef-4897-9ec4-b3008a7d5264
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetCustomAttributeProps, GetCustomAttributeProps method [Windows Runtime], GetCustomAttributeProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetCustomAttributeProps method, IMetaDataImport.GetCustomAttributeProps, IMetaDataImport::GetCustomAttributeProps, rometadataapi/IMetaDataImport::GetCustomAttributeProps, winrt.imetadataimport_getcustomattributeprops
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.GetCustomAttributeProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport::GetCustomAttributeProps


## -description


Gets the value of the custom attribute, given its metadata token.


## -parameters




### -param cv [in]

A metadata token that represents the custom attribute to be retrieved.


### -param ptkObj [out]

A metadata token representing the object that the custom attribute modifies. This value can be any type of metadata token except <b>mdCustomAttribute</b>. See <a href="http://msdn.microsoft.com/en-us/library/ms404456.aspx">Metadata Tokens</a> for more information about the token types.


### -param ptkType [out]

An <b>mdMethodDef</b> or <b>mdMemberRef</b> metadata token representing the Type of the returned custom attribute.


### -param ppBlob




### -param pcbBlob [out]

The size in bytes of the data returned in <i>const</i>.


#### - const [out]

A pointer to an array of data that is the value of the custom attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A custom attribute is stored as an array of data, the format of which is understood by the metadata engine.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

