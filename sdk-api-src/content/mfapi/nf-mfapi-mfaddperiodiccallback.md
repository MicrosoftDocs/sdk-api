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

# MFAddPeriodicCallback function


## -description



Sets a callback function to be called at a fixed interval.




## -parameters




### -param Callback [in]

Pointer to the callback function, of type <a href="https://msdn.microsoft.com/9449fa04-867c-4f27-a05c-ff0d6e912c53">MFPERIODICCALLBACK</a>.


### -param pContext [in]

Pointer to a caller-provided object that implements <b>IUnknown</b>, or <b>NULL</b>. This parameter is passed to the callback function.


### -param pdwKey [out]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="https://msdn.microsoft.com/e70cdad3-c330-4368-8ef8-d616157b5e72">MFRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



To get the timer interval for the periodic callback, call <a href="https://msdn.microsoft.com/19d7ae7e-7ae3-474d-8111-3b60b9adb918">MFGetTimerPeriodicity</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

