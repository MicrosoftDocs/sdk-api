---
UID: NN:comsvcs.ICrmLogControl
title: ICrmLogControl
author: windows-sdk-content
description: Is the means by which the CRM Worker and CRM Compensator write records to the log and make them durable.
old-location: cos\icrmlogcontrol.htm
tech.root: cossdk
ms.assetid: 3309ed58-8161-46f3-93bc-afc0c9bc8d50
ms.author: windowssdkdev
ms.date: 12/5/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmLogControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICrmLogControl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms681306(v=VS.85).aspx">ForceLog</a>
</td>
<td align="left" width="63%">
Forces all log records to be durable on disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681714(v=VS.85).aspx">ForceTransactionToAbort</a>
</td>
<td align="left" width="63%">
Performs an immediate abort call on the transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686114(v=VS.85).aspx">ForgetLogRecord</a>
</td>
<td align="left" width="63%">
Forgets the last log record written by this instance of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679831(v=VS.85).aspx">get_TransactionUOW</a>
</td>
<td align="left" width="63%">
Retrieves the transaction unit of work (UOW) without having to log the transaction UOW in the log record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688384(v=VS.85).aspx">RegisterCompensator</a>
</td>
<td align="left" width="63%">
The CRM Worker uses this method to register the CRM Compensator with the CRM infrastructure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686002(v=VS.85).aspx">WriteLogRecord</a>
</td>
<td align="left" width="63%">
The CRM Worker and CRM Compensator use this method to write unstructured log records to the log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687711(v=VS.85).aspx">WriteLogRecordVariants</a>
</td>
<td align="left" width="63%">
The CRM Worker and CRM Compensator use this method to write structured log records to the log.

</td>
</tr>
</table> 


## -remarks



The CRM Compensator receives this interface after its instantiation using the <a href="https://msdn.microsoft.com/en-us/library/ms685163(v=VS.85).aspx">ICrmCompensator::SetLogControl</a> or the <a href="https://msdn.microsoft.com/en-us/library/ms681730(v=VS.85).aspx">ICrmCompensatorVariants::SetLogControlVariants</a> method.

In addition to the return values listed for each method, the methods can also return error codes from the Distributed Transaction Coordinator (DTC) or other standard COM error codes.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>
 

 

