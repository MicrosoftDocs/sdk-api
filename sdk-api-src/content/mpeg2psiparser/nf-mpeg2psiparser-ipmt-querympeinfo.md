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

# IPMT::QueryMPEInfo


## -description



The <b>QueryMPEInfo</b> method returns the multi-protocol encapsulation (MPE) information in the PMT, if any.




## -parameters




### -param ppMPEList [out]

Address of a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/2753160b-de52-4d62-960a-c200c6f5f29a">MPE_ELEMENT</a> structures. The client must free the array by calling the <b>CoTaskMemFree</b> function.


### -param puiCount [out]

Receives the number of elements returned in <i>ppMPEList</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
Malformed table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was found in the PMT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was not found in the PMT.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, it returns one of the two success codes listed in the previous table. It returns MPEG2_S_MPE_INFO_FOUND if the PMT contains MPE information, or MPEG2_S_MPE_INFO_NOT_FOUND if the PMT does not contain any MPE information.




## -see-also




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

