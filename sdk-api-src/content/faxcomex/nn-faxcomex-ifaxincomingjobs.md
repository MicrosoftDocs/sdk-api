---
UID: NN:faxcomex.IFaxIncomingJobs
title: IFaxIncomingJobs
author: windows-sdk-content
description: The IFaxIncomingJobs interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a FaxIncomingJob object.
old-location: fax\_mfax_faxincomingjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_28vn_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxIncomingJobs, IFaxIncomingJobs interface [Fax Service], IFaxIncomingJobs interface [Fax Service],described, _mfax_faxincomingjobs_cpp, fax._mfax_faxincomingjobs_cpp, faxcomex/IFaxIncomingJobs
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
 - IFaxIncomingJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJobs interface


## -description


The <b>IFaxIncomingJobs</b> interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object.

The <b>IFaxIncomingJobs</b> interface is accessed through the <a href="https://msdn.microsoft.com/291f8709-c10f-4041-864f-82431edd7fab">IFaxIncomingQueue</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJobs</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingJobs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingJobs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7827f5b-68f9-4b2d-9a88-a0dcf933a041">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d7827f5b-68f9-4b2d-9a88-a0dcf933a041">get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6d1dbb5-7019-4a84-8118-4aff00a87b1b">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object from the <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJobs</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17d63c5f-2aa7-48fc-9a35-7c3ff36e0d69">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/17d63c5f-2aa7-48fc-9a35-7c3ff36e0d69">Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> collection. This is the total number of incoming jobs for the fax server.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingJobs</b> object in C++, call the <a href="https://msdn.microsoft.com/c739a92b-4b3e-4ab5-8b17-4bc4db19ed0b">IFaxIncomingQueue::GetJobs</a> method.




## -see-also




<a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/291f8709-c10f-4041-864f-82431edd7fab">IFaxIncomingQueue</a>
 

 

