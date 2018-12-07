---
UID: NN:comsvcs.ICrmMonitorClerks
title: ICrmMonitorClerks
author: windows-sdk-content
description: Retrieves information about the state of clerks.
old-location: cos\icrmmonitorclerks.htm
tech.root: cossdk
ms.assetid: 90403516-f677-4396-8991-ae621c159567
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICrmMonitorClerks, ICrmMonitorClerks interface [COM+], ICrmMonitorClerks interface [COM+],described, _dtc_ICrmMonitorClerks_Interface, comsvcs/ICrmMonitorClerks, cos.icrmmonitorclerks
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
 - ICrmMonitorClerks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmMonitorClerks interface


## -description


Retrieves information about the state of clerks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmMonitorClerks</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICrmMonitorClerks</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICrmMonitorClerks</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679206(v=VS.85).aspx">ActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the activity ID of the CRM Worker for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679835(v=VS.85).aspx">Description</a>
</td>
<td align="left" width="63%">
Retrieves the description of the CRM Compensator for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686087(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the instance CLSIDs of the CRM clerks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681812(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the count of CRM clerks in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685206(v=VS.85).aspx">Item</a>
</td>
<td align="left" width="63%">
Retrieves the instance CLSID of the CRM clerk for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686113(v=VS.85).aspx">ProgIdCompensator</a>
</td>
<td align="left" width="63%">
Retrieves the ProgId of the CRM Compensator for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684336(v=VS.85).aspx">TransactionUOW</a>
</td>
<td align="left" width="63%">
Retrieves the unit of work (UOW) of the transaction for the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>
 

 

