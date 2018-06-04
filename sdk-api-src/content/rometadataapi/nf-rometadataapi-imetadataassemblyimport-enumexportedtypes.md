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

# IMetaDataAssemblyImport::EnumExportedTypes


## -description


Enumerates the exported types referenced in the assembly manifest in the current metadata scope.


## -parameters




### -param phEnum [in, out]

 A pointer to the enumerator. This must be a null value when the <b>EnumExportedTypes</b> method is called for the first time.


### -param rExportedTypes [out]

The enumeration of <b>mdExportedType</b> metadata tokens.


### -param cMax [in]

The maximum number of <b>mdExportedType</b> tokens that can be placed in the <i>rExportedTypes</i> array.




### -param pcTokens [out]

The number of <b>mdExportedType</b> tokens actually placed in <i>rExportedTypes</i>.




## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumExportedTypes</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

