---
UID: NN:faxcomex.IFaxAccountOutgoingQueue
title: IFaxAccountOutgoingQueue (faxcomex.h)
author: windows-sdk-content
description: Used by a fax client application to retrieve the outbound fax jobs (FaxOutgoingJobs object) in the job queue for a particular fax account.
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\faxinta_n_ifaxaccountoutgoingqueue_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxAccountOutgoingQueue, IFaxAccountOutgoingQueue interface [Fax Service], IFaxAccountOutgoingQueue interface [Fax Service],described, _mfax_faxaccountoutgoingqueue_cpp, fax._mfax_faxaccountoutgoingqueue_cpp, faxcomex/IFaxAccountOutgoingQueue
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxAccountOutgoingQueue"
dev_langs:
 - c++
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
 - IFaxAccountOutgoingQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxAccountOutgoingQueue interface


## -description


Used by a fax client application to retrieve the outbound fax jobs (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountOutgoingQueue</b> interface is accessed through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountfolders">IFaxAccountFolders</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingQueue</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxAccountOutgoingQueue</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingqueue-getjob-vb">GetJob</a>
</td>
<td align="left" width="63%">
Returns an outgoing fax job in the job queue of the current fax account according to the job's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingqueue-getjobs-vb">GetJobs</a>
</td>
<td align="left" width="63%">
Returns the collection of outbound fax jobs in the queue for the current fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingqueue">FaxAccountOutgoingQueue</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountfolders">IFaxAccountFolders</a>
 

 

