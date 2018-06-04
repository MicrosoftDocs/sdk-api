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

# IMetaDataImport::EnumUnresolvedMethods


## -description


Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param rgMethods [out]

The array used to store the MemberDef tokens.


### -param cMax [in]

The maximum size of the <i>rgMethods</i> array.


### -param pcTokens [out]

The number of MemberDef tokens returned in <i>rgMethods</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumUnresolvedMethods</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



An unresolved method is one that has been declared but not implemented. A method is included in the enumeration if the method is marked <b>miForwardRef</b> and either <b>mdPinvokeImpl</b> or <b>miRuntime</b> is set to zero. In other words, an unresolved method is a class method that is marked <b>miForwardRef</b> but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself. 



The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

