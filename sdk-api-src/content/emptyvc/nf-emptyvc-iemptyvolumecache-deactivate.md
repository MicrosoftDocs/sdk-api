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

# IEmptyVolumeCache::Deactivate


## -description


Notifies the handler that the disk cleanup manager is shutting down. 


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

A flag that can be set to return information to the disk cleanup manager. It can have the following value. 



#### EVCF_REMOVEFROMLIST

If this flag is set, the disk cleanup manager will delete the handler's registry subkey. 


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
This value should always be returned.

</td>
</tr>
</table>
 




## -remarks



If the <b>EVCF_REMOVEFROMLIST</b> flag is set, the handler will not be run again unless the registry entries are reestablished. This flag is typically used for a handler that will only run once.



