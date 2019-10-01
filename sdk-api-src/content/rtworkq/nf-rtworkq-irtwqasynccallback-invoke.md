---
UID: NF:rtworkq.IRtwqAsyncCallback.Invoke
title: IRtwqAsyncCallback::Invoke (rtworkq.h)
author: windows-sdk-content
description: Called when an asynchronous operation is completed.
old-location: base\irtwqasynccallback_invoke.htm
tech.root: ProcThread
ms.assetid: 1798C338-4C82-42A7-AE15-ADFD356604BD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRtwqAsyncCallback interface,Invoke method, IRtwqAsyncCallback.Invoke, IRtwqAsyncCallback::Invoke, Invoke, Invoke method, Invoke method,IRtwqAsyncCallback interface, base.irtwqasynccallback_invoke, rtworkq/IRtwqAsyncCallback::Invoke
ms.topic: method
f1_keywords: 
 - "rtworkq/IRtwqAsyncCallback.Invoke"
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncCallback.Invoke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRtwqAsyncCallback::Invoke


## -description



Called when an asynchronous operation is completed.




## -parameters




### -param pAsyncResult [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a> interface. Pass this pointer to the asynchronous <b>End...</b> method to complete the asynchronous call.


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



Within your implementation of <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cdeferredcommand-invoke">Invoke</a>, call the corresponding <b>End...</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasynccallback">IRtwqAsyncCallback</a>
 

 

