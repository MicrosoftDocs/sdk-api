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

# IMetaDataImport2::EnumMethodSpecs


## -description


Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.


## -parameters




### -param phEnum [in, out]

 pointer to the enumerator for <i>rMethodSpecs</i>.


### -param tk [in]

The <b>MemberRef</b> or <b>MethodDef</b> token that represents the method whose <b>MethodSpec</b> tokens are to be enumerated. If the value of <i>tk</i> is 0 (zero), all <b>MethodSpec</b> tokens in the scope will be enumerated.


### -param rMethodSpecs [out]

The array of <b>MethodSpec</b> tokens to enumerate.


### -param cMax [in]

The requested maximum number of tokens to place in <i>rMethodSpecs</i>.


### -param pcMethodSpecs [out]

The returned number of tokens placed in <i>rMethodSpecs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodSpecs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcMethodSpecs</i> is set to 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

