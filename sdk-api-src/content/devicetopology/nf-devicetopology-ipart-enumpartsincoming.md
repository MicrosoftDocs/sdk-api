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

# IPart::EnumPartsIncoming


## -description



The <b>EnumPartsIncoming</b> method gets a list of all the incoming parts—that is, the parts that reside on data paths that are upstream from this part.




## -parameters




### -param ppParts [out]

Pointer to a pointer variable into which the method writes the address of an <a href="https://msdn.microsoft.com/3ac48781-90c2-4b23-aa68-3453091bde61">IPartsList</a> interface that encapsulates the list of parts that are immediately upstream from this part. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>EnumPartsIncoming</b> call fails,  <i>*ppParts</i> is <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppParts</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This part has no links to upstream parts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



A client application can traverse a device topology against the direction of audio data flow by iteratively calling this method at each step in the traversal to get the list of parts that lie immediately upstream from the current part.

If this part has no links to upstream parts, the method returns error code E_NOTFOUND and does not create a parts list (<i>*ppParts</i> is <b>NULL</b>). For example, the method returns this error code if the <b>IPart</b> interface represents a connector through which data enters a device topology.




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/3ac48781-90c2-4b23-aa68-3453091bde61">IPartsList Interface</a>
 

 

