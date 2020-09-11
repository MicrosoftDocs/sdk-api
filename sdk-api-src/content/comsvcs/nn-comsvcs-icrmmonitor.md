---
UID: NN:comsvcs.ICrmMonitor
title: ICrmMonitor (comsvcs.h)
description: Captures a snapshot of the current state of the CRM and holds a specific CRM clerk.
helpviewer_keywords: ["ICrmMonitor","ICrmMonitor interface [COM+]","ICrmMonitor interface [COM+]","described","_dtc_ICrmMonitor_Interface","comsvcs/ICrmMonitor","cos.icrmmonitor"]
old-location: cos\icrmmonitor.htm
tech.root: cos
ms.assetid: ead5f782-8512-4387-b8f3-7be960f35bbe
ms.date: 12/05/2018
ms.keywords: ICrmMonitor, ICrmMonitor interface [COM+], ICrmMonitor interface [COM+],described, _dtc_ICrmMonitor_Interface, comsvcs/ICrmMonitor, cos.icrmmonitor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmMonitor
 - comsvcs/ICrmMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitor
---

# ICrmMonitor interface


## -description

Captures a snapshot of the current state of the CRM and holds a specific CRM clerk.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmMonitor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmMonitor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmmonitor-getclerks">GetClerks</a>
</td>
<td align="left" width="63%">
Retrieves a clerk collection object, which is a snapshot of the current state of the clerks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmmonitor-holdclerk">HoldClerk</a>
</td>
<td align="left" width="63%">
Retrieves a pointer on the specified clerk.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a>

