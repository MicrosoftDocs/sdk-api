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

# ISyncMgrSynchronizeCallback::ShowPropertiesCompleted


## -description


Called by the registered application's handler before or after its 
<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> operation is completed.


## -parameters




### -param hr






#### - hrResult [in]

Type: <b>HRESULT</b>

Whether the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> was successful.


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
Call was completed successfully.

</td>
</tr>
</table>
 




## -remarks



It is acceptable for the registered application's handler to call this method before returning from the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> method.

This method should not be called if the registered application's handler does not return a success code from the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a>
 

 

