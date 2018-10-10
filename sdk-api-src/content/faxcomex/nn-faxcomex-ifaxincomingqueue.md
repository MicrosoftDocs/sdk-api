---
UID: NN:faxcomex.IFaxIncomingQueue
title: IFaxIncomingQueue
author: windows-sdk-content
description: The IFaxIncomingQueue interface is used by a fax client application to manage the inbound fax jobs (FaxIncomingJobs object) in the job queue. The object also includes a method to block inbound faxes from the fax job queue.
old-location: fax\_mfax_faxincomingqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4x7p_cpp.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxIncomingQueue, IFaxIncomingQueue interface [Fax Service], IFaxIncomingQueue interface [Fax Service],described, _mfax_faxincomingqueue_cpp, fax._mfax_faxincomingqueue_cpp, faxcomex/IFaxIncomingQueue
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
 - IFaxIncomingQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingQueue interface


## -description


The <b>IFaxIncomingQueue</b> interface is used by a fax client application to manage the inbound fax jobs (<a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> object) in the job queue. The object also includes a method to block inbound faxes from the fax job queue.

The <b>IFaxIncomingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/98e650c7-fc8e-4bf3-91ca-d9dc2ab09f50">IFaxFolders</a> interface.
<div class="alert"><b>Note</b>  Changes made to the <b>FaxIncomingQueue</b> object will not be saved until you call the <a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">Save</a> method.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingQueue</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b545785-f237-4a36-9b9c-1eca4e4daaa4">GetJob</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6b545785-f237-4a36-9b9c-1eca4e4daaa4">GetJob</a> method returns an incoming fax job in the job queue according to its ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c739a92b-4b3e-4ab5-8b17-4bc4db19ed0b">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c739a92b-4b3e-4ab5-8b17-4bc4db19ed0b">GetJobs</a> method returns the collection of inbound fax jobs in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23626ea8-e2e8-4592-a930-f4be7b8f88d0">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/23626ea8-e2e8-4592-a930-f4be7b8f88d0">Refresh</a> method refreshes <a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">Save</a> method saves the <a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a> object's data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingQueue</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/65345e37-996a-40e4-a43b-38dbf94fe24f">Blocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/65345e37-996a-40e4-a43b-38dbf94fe24f">Blocked</a> property is a Boolean value that indicates whether the job queue for incoming faxes is blocked. 

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingQueue</b> object in C++, call the <a href="https://msdn.microsoft.com/3e29e5dd-bbb0-4ea3-9f1d-44df674febd8">IFaxFolders::get_IncomingQueue</a> method.




## -see-also




<a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/98e650c7-fc8e-4bf3-91ca-d9dc2ab09f50">IFaxFolders</a>



<a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">IFaxIncomingQueue::Save</a>
 

 

