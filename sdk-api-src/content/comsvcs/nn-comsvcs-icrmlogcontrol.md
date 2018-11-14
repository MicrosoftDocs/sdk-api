---
UID: NN:comsvcs.ICrmLogControl
title: ICrmLogControl
author: windows-sdk-content
description: Is the means by which the CRM Worker and CRM Compensator write records to the log and make them durable.
old-location: cos\icrmlogcontrol.htm
tech.root: cossdk
ms.assetid: 3309ed58-8161-46f3-93bc-afc0c9bc8d50
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICrmLogControl, ICrmLogControl interface [COM+], ICrmLogControl interface [COM+],described, _dtc_ICrmLogControl_Interface, comsvcs/ICrmLogControl, cos.icrmlogcontrol
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICrmLogControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmLogControl interface


## -description


Is the means by which the CRM Worker and CRM Compensator write records to the log and make them durable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmLogControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmLogControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICrmLogControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/547c9e31-62a0-413e-8371-20356bfe8906">ForceLog</a>
</td>
<td align="left" width="63%">
Forces all log records to be durable on disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a0289c6-d177-40a3-968d-96ae3179e78d">ForceTransactionToAbort</a>
</td>
<td align="left" width="63%">
Performs an immediate abort call on the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1871ca0-0586-41de-9684-2babaafe8796">ForgetLogRecord</a>
</td>
<td align="left" width="63%">
Forgets the last log record written by this instance of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35cfadf5-f1be-4383-bb34-f68543df0abb">get_TransactionUOW</a>
</td>
<td align="left" width="63%">
Retrieves the transaction unit of work (UOW) without having to log the transaction UOW in the log record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">RegisterCompensator</a>
</td>
<td align="left" width="63%">
The CRM Worker uses this method to register the CRM Compensator with the CRM infrastructure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2cbd9dc-5451-4aae-b2ce-28b2b93fd465">WriteLogRecord</a>
</td>
<td align="left" width="63%">
The CRM Worker and CRM Compensator use this method to write unstructured log records to the log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd3943d-0c77-49fe-a53e-bc0c45e13a54">WriteLogRecordVariants</a>
</td>
<td align="left" width="63%">
The CRM Worker and CRM Compensator use this method to write structured log records to the log.

</td>
</tr>
</table> 


## -remarks



The CRM Compensator receives this interface after its instantiation using the <a href="https://msdn.microsoft.com/a68e49c7-a0d3-4c37-b438-864578e4a680">ICrmCompensator::SetLogControl</a> or the <a href="https://msdn.microsoft.com/5cf602fb-b5b9-471b-b617-9df6725eaf35">ICrmCompensatorVariants::SetLogControlVariants</a> method.

In addition to the return values listed for each method, the methods can also return error codes from the Distributed Transaction Coordinator (DTC) or other standard COM error codes.




## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>
 

 

