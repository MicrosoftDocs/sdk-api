---
UID: NF:mfapi.MFScheduleWorkItemEx
title: MFScheduleWorkItemEx function
author: windows-sdk-content
description: Schedules an asynchronous operation to be completed after a specified interval.
old-location: mf\mfscheduleworkitemex.htm
tech.root: MedFound
ms.assetid: b698cae1-4f3b-4649-b6f7-583f223eb90c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFScheduleWorkItemEx, MFScheduleWorkItemEx function [Media Foundation], b698cae1-4f3b-4649-b6f7-583f223eb90c, mf.mfscheduleworkitemex, mfapi/MFScheduleWorkItemEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFScheduleWorkItemEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFScheduleWorkItemEx function


## -description



Schedules an asynchronous operation to be completed after a specified interval.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a>.


### -param Timeout [in]

Time-out interval, in milliseconds. Set this parameter to a negative value. The callback is invoked after −<i>Timeout</i> milliseconds. For example, if <i>Timeout</i> is −5000, the callback is invoked after 5000 milliseconds.


### -param pKey [out]

Receives a key that can be used to cancel the timer. To cancel the timer, call <a href="https://msdn.microsoft.com/a24fae61-30c8-4aca-b067-22b99f904fd8">MFCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.


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



When the timer interval elapses, the timer calls <a href="https://msdn.microsoft.com/28832d50-9b15-4eb0-96f9-2032d4edcaf4">MFInvokeCallback</a> with the <i>pResult</i> pointer to invoke the asynchronous callback. The callback is specified when you create the result object.




## -see-also




<a href="https://msdn.microsoft.com/c14786e4-7fbe-4748-a6ba-e9e68f78b241">MFScheduleWorkItem</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

