---
UID: NF:rometadataapi.IMetaDataImport.GetCustomAttributeByName
title: IMetaDataImport::GetCustomAttributeByName
author: windows-sdk-content
description: Gets the custom attribute, given its name and owner.
old-location: winrt\imetadataimport_getcustomattributebyname.htm
old-project: WinRT
ms.assetid: e2771a90-4ac3-4c5a-869a-e18d1a4c6b3e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCustomAttributeByName, GetCustomAttributeByName method [Windows Runtime], GetCustomAttributeByName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetCustomAttributeByName method, IMetaDataImport.GetCustomAttributeByName, IMetaDataImport::GetCustomAttributeByName, rometadataapi/IMetaDataImport::GetCustomAttributeByName, winrt.imetadataimport_getcustomattributebyname
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.GetCustomAttributeByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::GetCustomAttributeByName


## -description


Gets the custom attribute, given its name and owner.


## -parameters




### -param tkObj [in]

A metadata token representing the object that owns the custom attribute.


### -param szName [in]

The name of the custom attribute.


### -param ppData




### -param pcbData [out]

The size in bytes of the data returned in <i>const</i>.


#### - const [out]

A pointer to an array of data that is the value of the custom attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is legal to define multiple custom attributes for the same owner; they may even have the same name. However, <b>GetCustomAttributeByName</b> returns only one instance. (<b>GetCustomAttributeByName</b> returns the first instance that it encounters.) To find all instances of a custom attribute, call the <a href="https://msdn.microsoft.com/d5ecb71e-a52f-421b-aab9-48efcc77ec2f">EnumCustomAttributes</a> method.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

