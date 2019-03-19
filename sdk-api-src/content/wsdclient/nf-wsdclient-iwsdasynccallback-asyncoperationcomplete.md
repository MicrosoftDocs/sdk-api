---
UID: NF:wsdclient.IWSDAsyncCallback.AsyncOperationComplete
title: IWSDAsyncCallback::AsyncOperationComplete (wsdclient.h)
author: windows-sdk-content
description: Indicates that the asynchronous operation has completed.
old-location: ncd\iwsdasynccallback_asyncoperationcomplete_method.htm
tech.root: WsdApi
ms.assetid: f2272d1e-bb12-43cd-a0ae-80530ad25fcf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AsyncOperationComplete, AsyncOperationComplete method, AsyncOperationComplete method,IWSDAsyncCallback interface, IWSDAsyncCallback interface,AsyncOperationComplete method, IWSDAsyncCallback.AsyncOperationComplete, IWSDAsyncCallback::AsyncOperationComplete, ncd.iwsdasynccallback_asyncoperationcomplete_method, wsdclient/IWSDAsyncCallback::AsyncOperationComplete
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDAsyncCallback.AsyncOperationComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDAsyncCallback::AsyncOperationComplete


## -description


Indicates that the asynchronous operation has completed.


## -parameters




### -param pAsyncResult [in]

Pointer to an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object that contains the user-defined state information passed to <a href="https://msdn.microsoft.com/39fc05f8-4b09-4305-b9a4-b4ef65788efc">IWSDAsyncResult::SetCallback</a>.


### -param pAsyncState [in]

The state of the asynchronous operation.


## -returns



Possible return values include, but are not limited to, the following:

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



The value returned by <b>AsyncOperationComplete</b> is ignored.




## -see-also




<a href="https://msdn.microsoft.com/24108143-55b7-4098-a4cc-025dfdfd054a">IWSDAsyncCallback</a>
 

 

