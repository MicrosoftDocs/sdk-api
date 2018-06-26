---
UID: NF:rometadataapi.IMetaDataImport.EnumProperties
title: IMetaDataImport::EnumProperties
author: windows-sdk-content
description: Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.
old-location: winrt\imetadataimport_enumproperties.htm
old-project: WinRT
ms.assetid: 54b89188-43d3-4997-aef4-48beaae151da
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: EnumProperties, EnumProperties method [Windows Runtime], EnumProperties method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumProperties method, IMetaDataImport.EnumProperties, IMetaDataImport::EnumProperties, rometadataapi/IMetaDataImport::EnumProperties, winrt.imetadataimport_enumproperties
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
 - IMetaDataImport.EnumProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumProperties


## -description


Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param tkTypDef [in]

A TypeDef token representing the type with properties to enumerate.


### -param rgProperties [out]

The array used to store the PropertyDef tokens.


### -param cMax [in]

The maximum size of the <i>rgProperties</i> array.


### -param pcProperties [out]

The number of PropertyDef tokens returned in <i>rgProperties</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumProperties</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcProperties</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

