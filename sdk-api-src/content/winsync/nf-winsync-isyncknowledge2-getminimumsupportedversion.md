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

# ISyncKnowledge2::GetMinimumSupportedVersion


## -description


Gets the minimum supported version of <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> components that can be used with this object. 


## -parameters




### -param pVersion [out]

The minimum supported version of Microsoft Sync Framework components that can be used with this object.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This method is used only with synchronization sessions that use <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> components.</div>
<div> </div>
A knowledge object that has a version of <b>SYNC_SERIALIZATION_VERSION_V2</b> supports components that are compatible with Sync Framework 1.0 when the knowledge object contains only elements that are compatible with Sync Framework 1.0. In this situation, <b>GetMinSupportedVersion</b> returns a version of <b>SYNC_SERIALIZATION_VERSION_V1</b>.

For an overview of what is involved in building synchronization providers using  <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a>, see <a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>



<a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>



<a href="https://msdn.microsoft.com/4fdb7123-d8c8-4ed7-9009-0e772252bbb7">SYNC_SERIALIZATION_VERSION Enumeration</a>
 

 

