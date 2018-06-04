---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMetaDataImport::EnumInterfaceImpls


## -description


Enumerates MethodDef tokens representing interface implementations.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param td [in]

The token of the TypeDef whose MethodDef tokens representing interface implementations are to be enumerated.


### -param rImpls [out]

The array used to store the MethodDef tokens.


### -param cMax [in]

The maximum size of the <i>rImpls</i> array.


### -param pcImpls [out, retval]

The actual number of tokens returned in <i>rImpls</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumInterfaceImpls</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MethodDef tokens to enumerate. In this case, <i>pcImpls</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

