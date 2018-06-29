---
UID: NF:rometadataapi.IMetaDataImport.EnumFieldsWithName
title: IMetaDataImport::EnumFieldsWithName
author: windows-sdk-content
description: Enumerates FieldDef tokens of the specified type with the specified name.
old-location: winrt\imetadataimport_enumfieldswithname.htm
old-project: WinRT
ms.assetid: 6035f267-778d-4d7d-84eb-1081f33ff619
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: EnumFieldsWithName, EnumFieldsWithName method [Windows Runtime], EnumFieldsWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumFieldsWithName method, IMetaDataImport.EnumFieldsWithName, IMetaDataImport::EnumFieldsWithName, rometadataapi/IMetaDataImport::EnumFieldsWithName, winrt.imetadataimport_enumfieldswithname
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
 - IMetaDataImport.EnumFieldsWithName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumFieldsWithName


## -description


Enumerates FieldDef tokens of the specified type with the specified name.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tkTypeDef [in]

The token of the type whose fields are to be enumerated.


### -param szName [in]

The field name that limits the scope of the enumeration.


### -param rFields [out]

Array used to store the FieldDef tokens.


### -param cMax [in]

The maximum size of the <i>rFields</i> array.




### -param pcTokens [out]

The actual number of FieldDef tokens returned in <i>rFields</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumFieldsWithName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no fields to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



Unlike <a href="https://msdn.microsoft.com/c9f8f389-fdb2-404b-a24e-cf2cf119bf55">EnumFields</a>, <b>EnumFieldsWithName</b> discards all field tokens that do not have the specified name.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

