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

# INSNetSourceCreator::Initialize


## -description



The <b>Initialize</b> method prepares the network source creator for operations. You must call this method before calling any of the other methods in the <b>INSNetSourceCreator</b> interface.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate memory for an internal resource.

</td>
</tr>
</table>
 




## -remarks



When you are finished using the network source creator, you must call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method to ensure that all resources are released properly.




## -see-also




<a href="https://msdn.microsoft.com/39e692a6-fb68-447f-bd28-8d216776157a">INSNetSourceCreator Interface</a>



<a href="https://msdn.microsoft.com/746b2ffa-c5bc-4df0-84fd-c3f1395e0d3e">INSNetSourceCreator::Shutdown</a>
 

 

