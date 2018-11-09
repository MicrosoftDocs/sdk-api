---
UID: NN:faxcomex.IFaxOutgoingJobs
title: IFaxOutgoingJobs
author: windows-sdk-content
description: The IFaxOutgoingJobs interface describes a messaging collection that is used by a fax client application to manage the outbound fax jobs in a fax server's job queue. Each outbound job is represented by a IFaxOutgoingJob interface.
old-location: fax\_mfax_faxoutgoingjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62yb_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IFaxOutgoingJobs interface


## -description


The <b>IFaxOutgoingJobs</b> interface describes a messaging collection that is used by a fax client application to manage the outbound fax jobs in a fax server's job queue. Each outbound job is represented by a <a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJobs</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutgoingJobs</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d8293335-172e-4440-a7da-3e1f38a7e0b7">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d8293335-172e-4440-a7da-3e1f38a7e0b7">IFaxOutgoingJobs::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <b>IFaxOutgoingJobs</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c0077a4-7b80-454e-885b-c78ff3e94f26">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6c0077a4-7b80-454e-885b-c78ff3e94f26">IFaxOutgoingJobs::get_Item</a> method returns a <a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a> interface from the <b>IFaxOutgoingJobs</b> interface.

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

<a href="https://msdn.microsoft.com/904de452-446a-4dbf-9d32-b83f26a715bf">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/904de452-446a-4dbf-9d32-b83f26a715bf">IFaxOutgoingJobs::get_Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a> collection. This is the total number of outgoing jobs for the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingJobs</b> is provided as the <a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a> object.



