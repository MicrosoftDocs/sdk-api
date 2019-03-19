---
UID: NN:comsvcs.ICrmMonitor
title: ICrmMonitor (comsvcs.h)
author: windows-sdk-content
description: Captures a snapshot of the current state of the CRM and holds a specific CRM clerk.
old-location: cos\icrmmonitor.htm
tech.root: cossdk
ms.assetid: ead5f782-8512-4387-b8f3-7be960f35bbe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICrmMonitor, ICrmMonitor interface [COM+], ICrmMonitor interface [COM+],described, _dtc_ICrmMonitor_Interface, comsvcs/ICrmMonitor, cos.icrmmonitor
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmMonitor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmMonitor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/b5802d3b-1464-4ddf-b459-a308b699de96">GetClerks</a>
</td>
<td align="left" width="63%">
Retrieves a clerk collection object, which is a snapshot of the current state of the clerks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e0f5197-d423-4b74-aaa1-2ec60e01d75c">HoldClerk</a>
</td>
<td align="left" width="63%">
Retrieves a pointer on the specified clerk.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/90403516-f677-4396-8991-ae621c159567">ICrmMonitorClerks</a>
 

 

