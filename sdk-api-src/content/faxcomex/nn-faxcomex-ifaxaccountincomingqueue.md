---
UID: NN:faxcomex.IFaxAccountIncomingQueue
title: IFaxAccountIncomingQueue (faxcomex.h)
description: Used by a fax client application to retrieve the inbound fax jobs (FaxIncomingJobs object) in the job queue for a particular fax account.
helpviewer_keywords: ["IFaxAccountIncomingQueue","IFaxAccountIncomingQueue interface [Fax Service]","IFaxAccountIncomingQueue interface [Fax Service]","described","_mfax_faxaccountincomingqueue_cpp","fax._mfax_faxaccountincomingqueue_cpp","faxcomex/IFaxAccountIncomingQueue"]
old-location: fax\_mfax_faxaccountincomingqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\faxinta_n_ifaxaccountincomingqueue_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountIncomingQueue, IFaxAccountIncomingQueue interface [Fax Service], IFaxAccountIncomingQueue interface [Fax Service],described, _mfax_faxaccountincomingqueue_cpp, fax._mfax_faxaccountincomingqueue_cpp, faxcomex/IFaxAccountIncomingQueue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxAccountIncomingQueue
 - faxcomex/IFaxAccountIncomingQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxAccountIncomingQueue
---

# IFaxAccountIncomingQueue interface


## -description

Used by a fax client application to retrieve the inbound fax jobs (<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountIncomingQueue</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountfolders">IFaxAccountFolders</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingQueue</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxAccountIncomingQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxAccountIncomingQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingqueue-getjob-vb">GetJob</a>
</td>
<td align="left" width="63%">
Returns an incoming fax job in the job queue of the current fax account according to the job's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingqueue-getjobs-vb">GetJobs</a>
</td>
<td align="left" width="63%">
Returns the collection of inbound fax jobs in the queue for the current fax account.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingqueue">FaxAccountIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountfolders">IFaxAccountFolders</a>