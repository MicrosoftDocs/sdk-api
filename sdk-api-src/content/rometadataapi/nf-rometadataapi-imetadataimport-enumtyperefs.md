---
UID: NF:rometadataapi.IMetaDataImport.EnumTypeRefs
title: IMetaDataImport::EnumTypeRefs
author: windows-sdk-content
description: Enumerates TypeRef tokens defined in the current metadata scope.
old-location: winrt\imetadataimport_enumtyperefs.htm
old-project: WinRT
ms.assetid: 8d77548d-dfba-4be1-b19d-41b21ab3a112
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: EnumTypeRefs, EnumTypeRefs method [Windows Runtime], EnumTypeRefs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumTypeRefs method, IMetaDataImport.EnumTypeRefs, IMetaDataImport::EnumTypeRefs, rometadataapi/IMetaDataImport::EnumTypeRefs, winrt.imetadataimport_enumtyperefs
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
 - IMetaDataImport.EnumTypeRefs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::EnumTypeRefs


## -description


Enumerates TypeRef tokens defined in the current metadata scope.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param rgTypeRefs [out]

The array used to store the TypeRef tokens.


### -param cMax [in]

The maximum size of the <i>rgTypeRefs</i> array.


### -param pcTypeRefs [out, retval]

A pointer to the number of TypeRef tokens returned in <i>rgTypeRefs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeRefs </b>returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeRefs</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

