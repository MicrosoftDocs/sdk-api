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

# IVssExpressWriter::Register


## -description


Causes VSS to store the writer's metadata in the express writer metadata store.


## -parameters






## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
<dt>0x8004230DL</dt>
</dl>
</td>
<td width="60%">
Metadata has already been stored for this writer.

</td>
</tr>
</table>
 




## -remarks



Before using this method, the caller must have either used the <a href="https://msdn.microsoft.com/2b670278-4589-47b7-a9ad-a24187c39945">LoadMetadata</a> method to load the writer's metadata directly or used the <a href="https://msdn.microsoft.com/254f4a32-cb33-494e-8fb4-06ab1cc2b184">CreateMetadata</a> method to create a writer metadata object.




## -see-also




<a href="https://msdn.microsoft.com/debb0731-6e24-4320-8236-220e07ec37c3">IVssExpressWriter</a>
 

 

