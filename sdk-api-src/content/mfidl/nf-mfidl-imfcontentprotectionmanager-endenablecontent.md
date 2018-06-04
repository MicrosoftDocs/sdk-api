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

# IMFContentProtectionManager::EndEnableContent


## -description



Ends an asynchronous request to perform a content enabling action. This method is called by the protected media path (PMP) to complete an asynchronous call to <a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">IMFContentProtectionManager::BeginEnableContent</a>.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. This pointer is the same value that the application passed to the caller's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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
</table>
 




## -remarks



When the <a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">BeginEnableContent</a> method completes asynchronously, the application notifies the PMP by invoking the asynchronous callback. The PMP calls <b>EndEnableContent</b> on the application to get the result code. This method is called on the application's thread from inside the callback method. Therefore, it must not block the thread that invoked the callback.

The application must return the success or failure code of the asynchronous processing that followed the call to <a href="https://msdn.microsoft.com/2f422135-8e5f-41fb-a709-77636d1b451b">BeginEnableContent</a>.




## -see-also




<a href="https://msdn.microsoft.com/0dba0384-eac7-456a-af9f-86eb944cdb2e">IMFContentProtectionManager</a>
 

 

