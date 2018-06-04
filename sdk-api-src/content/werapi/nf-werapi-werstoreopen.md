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

# WerStoreOpen function


## -description


Opens the collection of stored error reports.


## -parameters




### -param repStoreType

TBD


### -param phReportStore

TBD




#### - store

A pointer to a report store. On a successful call, this will point to the retrieved report store.


#### - storeType

The type of report store to open. See Remarks for details.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

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
One of the arguments is not a valid value.

</td>
</tr>
</table>
 




## -remarks



A <i>storeType</i> value of <b>E_STORE_MACHINE_QUEUE</b> opens the queue of all error reports on the machine that have not yet been sent to Microsoft. A value of  <b>E_STORE_MACHINE_ARCHIVE</b> opens the store of error reports that have already been sent.

The Windows Error Report (WER) Store is the queue of error reports that have been marked to be sent to Microsoft but have not yet been uploaded. The upload of an error report can be postponed under a number of circumstances. The WerStore functions allow developers to access the stored reports and query the status of each one.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/C34FBA67-5267-471C-B1AA-87BFC5725831">WerStoreClose</a>



<a href="https://msdn.microsoft.com/E4732B60-BFBE-4916-83A6-5F031D267913">WerStoreGetFirstReportKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

