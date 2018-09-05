---
UID: NF:rometadataapi.IMetaDataImport.EnumTypeSpecs
title: IMetaDataImport::EnumTypeSpecs
author: windows-sdk-content
description: Enumerates TypeSpec tokens defined in the current metadata scope.
old-location: winrt\imetadataimport_enumtypespecs.htm
old-project: WinRT
ms.assetid: 81b3b750-b9bd-42f1-b49d-134a10493ae5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumTypeSpecs, EnumTypeSpecs method [Windows Runtime], EnumTypeSpecs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumTypeSpecs method, IMetaDataImport.EnumTypeSpecs, IMetaDataImport::EnumTypeSpecs, rometadataapi/IMetaDataImport::EnumTypeSpecs, winrt.imetadataimport_enumtypespecs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.redist: 
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
 - IMetaDataImport.EnumTypeSpecs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumTypeSpecs


## -description


Enumerates TypeSpec tokens defined in the current metadata scope.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This value must be NULL for the first call of this method.


### -param rgTypeSpecs [out]

The array used to store the TypeSpec tokens.


### -param cMax [in]

The maximum size of the <i>rgTypeSpecs</i> array.


### -param pcTypeSpecs [out]

The number of TypeSpec tokens returned in <i>rgTypeSpecs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeSpecs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeSpecs</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

