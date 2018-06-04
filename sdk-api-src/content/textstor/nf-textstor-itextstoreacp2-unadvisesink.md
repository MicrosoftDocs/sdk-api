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

# ITextStoreACP2::UnadviseSink


## -description


Called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.


## -parameters




### -param punk [in]

Pointer to a sink object. Cannot be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is no active sink object.

</td>
</tr>
</table>
 




## -remarks



Every call to the <a href="https://msdn.microsoft.com/15fa2f85-3fe8-4e2d-bd3b-a270182adc66">AdviseSink</a> method, which registers a new sink object, should be matched by a call to this method. Calls to the <b>AdviseSink</b> method that only update the <i>dwMask</i> parameter of a sink which was previously registered, do not require a call to the <b>UnadviseSink</b> method.

For example, to register a sink object, an application calls the <a href="https://msdn.microsoft.com/15fa2f85-3fe8-4e2d-bd3b-a270182adc66">AdviseSink</a> method the first time. After registering the sink object, the application can call the <b>AdviseSink</b> method again with the same sink object to change the <i>dwMask</i> parameter. To unregister the sink object, an application calls the <b>UnadviseSink</b> method.

The <i>punk</i> parameter must have the same COM identity as the pointer originally passed in the <a href="https://msdn.microsoft.com/15fa2f85-3fe8-4e2d-bd3b-a270182adc66">AdviseSink</a> method.




## -see-also




<a href="https://msdn.microsoft.com/15fa2f85-3fe8-4e2d-bd3b-a270182adc66">AdviseSink</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>
 

 

