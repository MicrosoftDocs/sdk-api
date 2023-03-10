---
UID: NF:rometadataapi.IMetaDataImport.GetCustomAttributeByName
title: IMetaDataImport::GetCustomAttributeByName (rometadataapi.h)
description: Gets the custom attribute, given its name and owner.
helpviewer_keywords: ["GetCustomAttributeByName","GetCustomAttributeByName method [Windows Runtime]","GetCustomAttributeByName method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetCustomAttributeByName method","IMetaDataImport.GetCustomAttributeByName","IMetaDataImport::GetCustomAttributeByName","rometadataapi/IMetaDataImport::GetCustomAttributeByName","winrt.imetadataimport_getcustomattributebyname"]
old-location: winrt\imetadataimport_getcustomattributebyname.htm
tech.root: WinRT
ms.assetid: e2771a90-4ac3-4c5a-869a-e18d1a4c6b3e
ms.date: 12/05/2018
ms.keywords: GetCustomAttributeByName, GetCustomAttributeByName method [Windows Runtime], GetCustomAttributeByName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetCustomAttributeByName method, IMetaDataImport.GetCustomAttributeByName, IMetaDataImport::GetCustomAttributeByName, rometadataapi/IMetaDataImport::GetCustomAttributeByName, winrt.imetadataimport_getcustomattributebyname
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
 - IMetaDataImport::GetCustomAttributeByName
 - rometadataapi/IMetaDataImport::GetCustomAttributeByName
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
 - IMetaDataImport.GetCustomAttributeByName
---

# IMetaDataImport::GetCustomAttributeByName


## -description

Gets the custom attribute, given its name and owner.

## -parameters

### -param tkObj [in]

A metadata token representing the object that owns the custom attribute.

### -param szName [in]

The name of the custom attribute.

### -param ppData [out]

A pointer to an array of data that is the value of the custom attribute.

### -param pcbData [out]

The size in bytes of the data returned in <i>const</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is legal to define multiple custom attributes for the same owner; they may even have the same name. However, <b>GetCustomAttributeByName</b> returns only one instance. (<b>GetCustomAttributeByName</b> returns the first instance that it encounters.) To find all instances of a custom attribute, call the <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumcustomattributes">EnumCustomAttributes</a> method.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>