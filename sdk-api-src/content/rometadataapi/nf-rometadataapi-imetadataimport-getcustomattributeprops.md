---
UID: NF:rometadataapi.IMetaDataImport.GetCustomAttributeProps
title: IMetaDataImport::GetCustomAttributeProps (rometadataapi.h)
description: Gets the value of the custom attribute, given its metadata token.
old-location: winrt\imetadataimport_getcustomattributeprops.htm
tech.root: WinRT
ms.assetid: ccb8891c-ceef-4897-9ec4-b3008a7d5264
ms.date: 12/05/2018
ms.keywords: GetCustomAttributeProps, GetCustomAttributeProps method [Windows Runtime], GetCustomAttributeProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetCustomAttributeProps method, IMetaDataImport.GetCustomAttributeProps, IMetaDataImport::GetCustomAttributeProps, rometadataapi/IMetaDataImport::GetCustomAttributeProps, winrt.imetadataimport_getcustomattributeprops
ms.topic: method
f1_keywords:
- rometadataapi/IMetaDataImport.GetCustomAttributeProps
dev_langs:
- c++
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
- IMetaDataImport.GetCustomAttributeProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::GetCustomAttributeProps


## -description


Gets the value of the custom attribute, given its metadata token.


## -parameters




### -param cv [in]

A metadata token that represents the custom attribute to be retrieved.


### -param ptkObj [out]

A metadata token representing the object that the custom attribute modifies. This value can be any type of metadata token except <b>mdCustomAttribute</b>. See <a href="https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms404456(v=vs.100)">Metadata Tokens</a> for more information about the token types.


### -param ptkType [out]

An <b>mdMethodDef</b> or <b>mdMemberRef</b> metadata token representing the Type of the returned custom attribute.


### -param ppBlob [out]

A pointer to an array of data that is the value of the custom attribute.


### -param pcbBlob [out]

The size in bytes of the data returned in <i>const</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A custom attribute is stored as an array of data, the format of which is understood by the metadata engine.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

