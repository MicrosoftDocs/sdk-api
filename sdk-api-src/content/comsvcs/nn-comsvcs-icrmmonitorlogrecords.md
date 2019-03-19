---
UID: NN:comsvcs.ICrmMonitorLogRecords
title: ICrmMonitorLogRecords (comsvcs.h)
author: windows-sdk-content
description: Monitors the individual log records maintained by a specific CRM clerk for a given transaction.
old-location: cos\icrmmonitorlogrecords.htm
tech.root: cossdk
ms.assetid: 5077ad2a-89c1-43f7-a7e0-7bd8036147b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICrmMonitorLogRecords, ICrmMonitorLogRecords interface [COM+], ICrmMonitorLogRecords interface [COM+],described, _dtc_ICrmMonitorLogRecords_Interface, comsvcs/ICrmMonitorLogRecords, cos.icrmmonitorlogrecords
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorLogRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmMonitorLogRecords interface


## -description


Monitors the individual log records maintained by a specific CRM clerk for a given transaction.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmMonitorLogRecords</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmMonitorLogRecords</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICrmMonitorLogRecords</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51acc910-a38a-4747-bf99-b468f7ffddd1">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of log records written by this CRM clerk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9b687c9-1e78-4896-a407-b069328ce66d">get_StructuredRecords</a>
</td>
<td align="left" width="63%">
Retrieves a flag indicating whether the log records written by this CRM clerk were structured.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9aaa3d6c-41b9-4661-8e7e-ef1d1abba4aa">get_TransactionState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5b566a-e98c-482d-9959-3498000875d3">GetLogRecord</a>
</td>
<td align="left" width="63%">
Retrieves an unstructured log record given its numeric index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f020d2d-ea2d-48c2-ab79-7b412e77b39f">GetLogRecordVariants</a>
</td>
<td align="left" width="63%">
Retrieves a structured log record given its numeric index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>
 

 

