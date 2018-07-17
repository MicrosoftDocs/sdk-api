---
UID: NF:rometadataapi.IMetaDataImport.EnumCustomAttributes
title: IMetaDataImport::EnumCustomAttributes
author: windows-sdk-content
description: Enumerates custom attribute-definition tokens associated with the specified type or member.
old-location: winrt\imetadataimport_enumcustomattributes.htm
old-project: WinRT
ms.assetid: d5ecb71e-a52f-421b-aab9-48efcc77ec2f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnumCustomAttributes, EnumCustomAttributes method [Windows Runtime], EnumCustomAttributes method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumCustomAttributes method, IMetaDataImport.EnumCustomAttributes, IMetaDataImport::EnumCustomAttributes, rometadataapi/IMetaDataImport::EnumCustomAttributes, winrt.imetadataimport_enumcustomattributes
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
 - IMetaDataImport.EnumCustomAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumCustomAttributes


## -description


Enumerates custom attribute-definition tokens associated with the specified type or member.


## -parameters




### -param phEnum [in, out]

A pointer to the returned enumerator.


### -param tk [in]

 A token for the scope of the enumeration, or zero for all custom attributes.


### -param tkType [in]

A token for the type of the attributes to be enumerated, or zero for all types.


### -param rgCustomAttributes [out]

An array of custom attribute tokens.


### -param cMax [in]

The maximum size of the <i>rgCustomAttributes</i> array.


### -param pcCustomAttributes [out]

The actual number of token values returned in <i>rgCustomAttributes</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumCustomAttributes</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no custom attributes to enumerate. In this case, <i>pcCustomAttributes</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

