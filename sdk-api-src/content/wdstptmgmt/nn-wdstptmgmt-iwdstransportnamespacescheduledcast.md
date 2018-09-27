---
UID: NN:wdstptmgmt.IWdsTransportNamespaceScheduledCast
title: IWdsTransportNamespaceScheduledCast
author: windows-sdk-content
description: Represents a base interface to the derived interfaces:\_IWdsTransportNamespaceScheduledCastManualStart and IWdsTransportNamespaceScheduledCastAutoStart.
old-location: wds\iwdstransportnamespacescheduledcast.htm
tech.root: wds
ms.assetid: 434e2eb2-b149-46e6-b7d0-0d07c44bcec2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IWdsTransportNamespaceScheduledCast, IWdsTransportNamespaceScheduledCast interface [Windows Deployment Services], IWdsTransportNamespaceScheduledCast interface [Windows Deployment Services],described, wds.iwdstransportnamespacescheduledcast, wdstptmgmt/IWdsTransportNamespaceScheduledCast
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespaceScheduledCast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportNamespaceScheduledCast interface


## -description


Represents a base interface to the derived interfaces: <a href="https://msdn.microsoft.com/ffbbdd4c-5d64-4ec0-a2f3-a5d31aec6402">IWdsTransportNamespaceScheduledCastManualStart</a> and <a href="https://msdn.microsoft.com/f11122a2-6ea9-4a73-ac93-0af7961f52b6">IWdsTransportNamespaceScheduledCastAutoStart</a>. An administrator must start  multicast sessions that are hosted by a namespace object of  these derived interfaces.   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespaceScheduledCast</b> interface inherits from <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>. <b>IWdsTransportNamespaceScheduledCast</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportNamespaceScheduledCast</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408ba96e-1a88-4a53-9cbe-8f2763542659">StartTransmission</a>
</td>
<td align="left" width="63%">
Starts a transmission on a namespace.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>
 

 

