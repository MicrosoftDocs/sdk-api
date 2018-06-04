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

# WsResetError function


## -description


Releases the content of the <i>error</i> object parameter but does not release the resource allocated to the <i>error</i> object parameter. 
            <div class="alert"><b>Note</b>  The "reset" effect of this function returns the <i>error</i> object to the state set at instantiation. The object is not released consequently is available for reuse.
            </div>
<div> </div>



## -parameters




### -param error [in]

This parameter is a   pointer to the <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object to reset.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks






                String data added to the error object using the <a href="https://msdn.microsoft.com/5fdad296-5024-4360-b1c5-f0192929c612">WsAddErrorString</a> function are released.
            

Properties that have been set using the  <a href="https://msdn.microsoft.com/5193eaf4-29f7-4e97-a3b0-97441b26399c">WsSetErrorProperty</a> function are released.
            



