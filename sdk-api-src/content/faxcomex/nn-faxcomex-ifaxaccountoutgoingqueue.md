---
UID: NN:faxcomex.IFaxAccountOutgoingQueue
title: IFaxAccountOutgoingQueue
author: windows-sdk-content
description: Used by a fax client application to retrieve the outbound fax jobs (FaxOutgoingJobs object) in the job queue for a particular fax account.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\faxinta_n_ifaxaccountoutgoingqueue_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
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


Used by a fax client application to retrieve the outbound fax jobs (<a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountOutgoingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/f7a60c42-55c8-43c1-acce-3b4f36a1d219">IFaxAccountFolders</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingQueue</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxAccountOutgoingQueue</b> also has these types of members:
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




<a href="https://msdn.microsoft.com/a1012b13-e629-4449-9b7c-c182dad56a9b">FaxAccountOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://msdn.microsoft.com/f7a60c42-55c8-43c1-acce-3b4f36a1d219">IFaxAccountFolders</a>
 

 

