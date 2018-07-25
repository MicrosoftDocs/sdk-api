---
UID: NN:faxcomex.IFaxOutgoingJobs
title: IFaxOutgoingJobs
author: windows-sdk-content
description: The IFaxOutgoingJobs interface describes a messaging collection that is used by a fax client application to manage the outbound fax jobs in a fax server's job queue. Each outbound job is represented by a IFaxOutgoingJob interface.
old-location: fax\_mfax_faxoutgoingjobs_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62yb_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxOutgoingJobs, IFaxOutgoingJobs interface [Fax Service], IFaxOutgoingJobs interface [Fax Service],described, _mfax_faxoutgoingjobs_cpp, fax._mfax_faxoutgoingjobs_cpp, faxcomex/IFaxOutgoingJobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJobs
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingJobs interface


## -description


The <b>IFaxOutgoingJobs</b> interface describes a messaging collection that is used by a fax client application to manage the outbound fax jobs in a fax server's job queue. Each outbound job is represented by a <a href="https://msdn.microsoft.com/library/ms689116(v=VS.85).aspx">IFaxOutgoingJob</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJobs</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxOutgoingJobs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingJobs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms688558(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms688558(v=VS.85).aspx">IFaxOutgoingJobs::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxOutgoingJobs</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms689514(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689514(v=VS.85).aspx">IFaxOutgoingJobs::get_Item</a> method returns a <a href="https://msdn.microsoft.com/library/ms689116(v=VS.85).aspx">IFaxOutgoingJob</a> interface from the <b>IFaxOutgoingJobs</b> interface.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJobs</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689537(v=VS.85).aspx">IFaxOutgoingJobs::get_Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a> collection. This is the total number of outgoing jobs for the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingJobs</b> is provided as the <a href="https://msdn.microsoft.com/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a> object.



