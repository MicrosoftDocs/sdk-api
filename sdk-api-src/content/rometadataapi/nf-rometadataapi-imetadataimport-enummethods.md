---
UID: NF:rometadataapi.IMetaDataImport.EnumMethods
title: IMetaDataImport::EnumMethods
author: windows-sdk-content
description: Enumerates MethodDef tokens representing methods of the specified type.
old-location: winrt\imetadataimport_enummethods.htm
tech.root: WinRT
ms.assetid: 3b0424d8-a0e3-4241-b957-d944e018cb31
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EnumMethods, EnumMethods method [Windows Runtime], EnumMethods method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMethods method, IMetaDataImport.EnumMethods, IMetaDataImport::EnumMethods, rometadataapi/IMetaDataImport::EnumMethods, winrt.imetadataimport_enummethods
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
 - IMetaDataImport.EnumMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rometadataapi.h
: 
- IMetaDataImport.EnumMethods
: 
---

# IMetaDataImport::EnumMethods


## -description


Enumerates MethodDef tokens representing methods of the specified type.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param tkTypeDef [in]

A TypeDef token representing the type with the methods to enumerate.


### -param rgMethods [out]

The array to store the MethodDef tokens.


### -param cMax [in]

The maximum size of the MethodDef <i>rgMethods</i> array.


### -param pcTokens [out]

The number of MethodDef tokens returned in <i>rgMethods</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethods</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MethodDef tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

