---
UID: NN:comsvcs.ICrmMonitor
title: ICrmMonitor
author: windows-sdk-content
description: Captures a snapshot of the current state of the CRM and holds a specific CRM clerk.
old-location: cos\icrmmonitor.htm
tech.root: cossdk
ms.assetid: ead5f782-8512-4387-b8f3-7be960f35bbe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICrmMonitor, ICrmMonitor interface [COM+], ICrmMonitor interface [COM+],described, _dtc_ICrmMonitor_Interface, comsvcs/ICrmMonitor, cos.icrmmonitor
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
 - ICrmMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmMonitor interface


## -description


Captures a snapshot of the current state of the CRM and holds a specific CRM clerk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmMonitor</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICrmMonitor</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICrmMonitor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686058(v=VS.85).aspx">GetClerks</a>
</td>
<td align="left" width="63%">
Retrieves a clerk collection object, which is a snapshot of the current state of the clerks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684177(v=VS.85).aspx">HoldClerk</a>
</td>
<td align="left" width="63%">
Retrieves a pointer on the specified clerk.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684207(v=VS.85).aspx">ICrmMonitorClerks</a>
 

 

