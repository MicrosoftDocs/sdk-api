---
UID: NF:wsdclient.IWSDAsyncResult.HasCompleted
title: IWSDAsyncResult::HasCompleted
author: windows-sdk-content
description: Indicates whether the operation has completed.
old-location: ncd\iwsdasyncresult_hascompleted_method.htm
old-project: WsdApi
ms.assetid: 67944519-c6cc-4dc8-9035-4e6ee84e1277
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: HasCompleted, HasCompleted method, HasCompleted method,IWSDAsyncResult interface, IWSDAsyncResult interface,HasCompleted method, IWSDAsyncResult.HasCompleted, IWSDAsyncResult::HasCompleted, ncd.iwsdasyncresult_hascompleted_method, wsdclient/IWSDAsyncResult::HasCompleted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.redist: 
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
 - IWSDAsyncResult.HasCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAsyncResult::HasCompleted


## -description


Indicates whether the operation has completed.


## -parameters






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
The operation completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation has not completed.

</td>
</tr>
</table>
 




## -remarks



A failed asynchronous operation is treated as a completed asynchronous operation. Error or fault information can be retrieved from the <a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a> interface using the <a href="https://msdn.microsoft.com/f2272d1e-bb12-43cd-a0ae-80530ad25fcf">IWSDAsyncCallback::AsyncOperationComplete</a> method.




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 

