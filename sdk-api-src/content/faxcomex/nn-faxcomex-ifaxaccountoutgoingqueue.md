---
UID: NN:faxcomex.IFaxAccountOutgoingQueue
title: IFaxAccountOutgoingQueue
author: windows-sdk-content
description: Used by a fax client application to retrieve the outbound fax jobs (FaxOutgoingJobs object) in the job queue for a particular fax account.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\faxinta_n_ifaxaccountoutgoingqueue_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxAccountOutgoingQueue, IFaxAccountOutgoingQueue interface [Fax Service], IFaxAccountOutgoingQueue interface [Fax Service],described, _mfax_faxaccountoutgoingqueue_cpp, fax._mfax_faxaccountoutgoingqueue_cpp, faxcomex/IFaxAccountOutgoingQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccountOutgoingQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccountOutgoingQueue interface


## -description


Used by a fax client application to retrieve the outbound fax jobs (<a href="https://msdn.microsoft.com/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountOutgoingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/library/Aa359052(v=VS.85).aspx">IFaxAccountFolders</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxAccountOutgoingQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxAccountOutgoingQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73500a95-5b8f-45fb-866a-b85a9018174c">GetJob</a>
</td>
<td align="left" width="63%">
Returns an outgoing fax job in the job queue of the current fax account according to the job's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c35e63af-9347-4951-aa9c-ee378cdc97e6">GetJobs</a>
</td>
<td align="left" width="63%">
Returns the collection of outbound fax jobs in the queue for the current fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/Aa358945(v=VS.85).aspx">FaxAccountOutgoingQueue</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/library/Aa359052(v=VS.85).aspx">IFaxAccountFolders</a>
 

 

