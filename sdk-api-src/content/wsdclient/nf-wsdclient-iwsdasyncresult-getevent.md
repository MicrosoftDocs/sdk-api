---
UID: NF:wsdclient.IWSDAsyncResult.GetEvent
title: IWSDAsyncResult::GetEvent
author: windows-sdk-content
description: Retrieves a WSD_EVENT structure that contains the result of the event.
old-location: ncd\iwsdasyncresult_getevent_method.htm
old-project: wsdapi
ms.assetid: de201c8b-9052-42f9-b95d-3b65cf0c86a3
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetEvent, GetEvent method, GetEvent method,IWSDAsyncResult interface, IWSDAsyncResult interface,GetEvent method, IWSDAsyncResult.GetEvent, IWSDAsyncResult::GetEvent, ncd.iwsdasyncresult_getevent_method, wsdclient/IWSDAsyncResult::GetEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDAsyncResult.GetEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAsyncResult::GetEvent


## -description


Retrieves a <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure that contains the result of the event.


## -parameters




### -param pEvent [out]

Reference to a <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure that provides data about the event. 



## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pEvent</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Event is not yet available or the asynchronous operation has not completed.

</td>
</tr>
</table>
 




## -remarks



This method should only be called by <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a> and only after the <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object has signaled that the operation has completed.




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 

