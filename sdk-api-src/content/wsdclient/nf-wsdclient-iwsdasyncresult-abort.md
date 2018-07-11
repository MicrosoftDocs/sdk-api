---
UID: NF:wsdclient.IWSDAsyncResult.Abort
title: IWSDAsyncResult::Abort
author: windows-sdk-content
description: Aborts the asynchronous operation.
old-location: ncd\iwsdasyncresult_abort.htm
old-project: wsdapi
ms.assetid: 9237bcb4-4404-4d15-a18a-1d651e3fb899
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: Abort, Abort method, Abort method,IWSDAsyncResult interface, IWSDAsyncResult interface,Abort method, IWSDAsyncResult.Abort, IWSDAsyncResult::Abort, ncd.iwsdasyncresult_abort, wsdclient/IWSDAsyncResult::Abort
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
 - IWSDAsyncResult.Abort
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAsyncResult::Abort


## -description


Aborts the asynchronous operation.


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
Method completed successfully.

</td>
</tr>
</table>
 




## -remarks



<b>Abort</b> waits for all pending callbacks set with <a href="https://msdn.microsoft.com/39fc05f8-4b09-4305-b9a4-b4ef65788efc">SetCallback</a> to complete before returning to the caller.




## -see-also




<a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a>
 

 

