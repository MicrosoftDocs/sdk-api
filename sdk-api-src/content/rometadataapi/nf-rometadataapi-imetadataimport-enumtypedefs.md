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

# IMetaDataImport::EnumTypeDefs


## -description


Enumerates TypeDef tokens representing all types within the current scope.


## -parameters




### -param phEnum [in, out]

A pointer to the new enumerator. This must be NULL for the first call of this method.


### -param rgTypeDefs [out]

The array used to store the TypeDef tokens.


### -param cMax [in]

The maximum size of the <i>rgTypeDefs</i> array.


### -param pcTypeDefs [out, retval]

The number of TypeDef tokens returned in <i>rgTypeDefs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeDefs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeDefs</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



The TypeDef token represents a type such as a class or an interface, as well as any type added via an extensibility mechanism.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

