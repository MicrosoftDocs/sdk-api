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


The <b>IFaxIncomingQueue</b> interface is used by a fax client application to manage the inbound fax jobs (<a href="https://msdn.microsoft.com/en-us/library/ms684959(v=VS.85).aspx">FaxIncomingJobs</a> object) in the job queue. The object also includes a method to block inbound faxes from the fax job queue.

The <b>IFaxIncomingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/en-us/library/ms684838(v=VS.85).aspx">IFaxFolders</a> interface.
<div class="alert"><b>Note</b>  Changes made to the <b>FaxIncomingQueue</b> object will not be saved until you call the <a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">Save</a> method.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxIncomingQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms686687(v=VS.85).aspx">GetJob</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686687(v=VS.85).aspx">GetJob</a> method returns an incoming fax job in the job queue according to its ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686761(v=VS.85).aspx">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686761(v=VS.85).aspx">GetJobs</a> method returns the collection of inbound fax jobs in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684944(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684944(v=VS.85).aspx">Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a> object's data.

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

<a href="https://msdn.microsoft.com/en-us/library/ms685101(v=VS.85).aspx">Blocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685101(v=VS.85).aspx">Blocked</a> property is a Boolean value that indicates whether the job queue for incoming faxes is blocked. 

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingQueue</b> object in C++, call the <a href="https://msdn.microsoft.com/en-us/library/ms686008(v=VS.85).aspx">IFaxFolders::get_IncomingQueue</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684838(v=VS.85).aspx">IFaxFolders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">IFaxIncomingQueue::Save</a>
 

 

