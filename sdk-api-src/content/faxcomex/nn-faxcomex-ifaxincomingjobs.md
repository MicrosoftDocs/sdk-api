---
UID: NN:faxcomex.IFaxIncomingJobs
title: IFaxIncomingJobs (faxcomex.h)
description: The IFaxIncomingJobs interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a FaxIncomingJob object.
helpviewer_keywords: ["IFaxIncomingJobs","IFaxIncomingJobs interface [Fax Service]","IFaxIncomingJobs interface [Fax Service]","described","_mfax_faxincomingjobs_cpp","fax._mfax_faxincomingjobs_cpp","faxcomex/IFaxIncomingJobs"]
old-location: fax\_mfax_faxincomingjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_28vn_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJobs, IFaxIncomingJobs interface [Fax Service], IFaxIncomingJobs interface [Fax Service],described, _mfax_faxincomingjobs_cpp, fax._mfax_faxincomingjobs_cpp, faxcomex/IFaxIncomingJobs
f1_keywords:
- faxcomex/IFaxIncomingJobs
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingJobs interface


## -description


The <b>IFaxIncomingJobs</b> interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object.

The <b>IFaxIncomingJobs</b> interface is accessed through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJobs</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingJobs</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjobs-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjobs-get__newenum">get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjobs-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> collection.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs-count-vb">Count</a> property represents the number of objects in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> collection. This is the total number of incoming jobs for the fax server.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingJobs</b> object in C++, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue-getjobs-vb">IFaxIncomingQueue::GetJobs</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>
 

 

