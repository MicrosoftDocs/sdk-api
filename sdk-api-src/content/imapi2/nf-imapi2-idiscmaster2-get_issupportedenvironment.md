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

# IDiscMaster2::get_IsSupportedEnvironment


## -description


Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices.


## -parameters




### -param value

Is VARIANT_TRUE if the environment contains one or more optical devices and the execution context has permission to access the devices; otherwise, VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



This method loops through all the strings in <a href="https://msdn.microsoft.com/e909acb9-850b-404d-a2f7-efb37faf3506">IDiscMaster2</a> and attempts to use each string to initialize a <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">DiscRecorder2</a> object.  If any of the recorders on the system succeed the initialization, this method returns <b>TRUE</b>.

The environment must contain at least one type-5 optical device.




## -see-also




<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>
 

 

