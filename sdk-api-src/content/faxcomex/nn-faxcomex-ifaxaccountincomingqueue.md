---
UID: NN:faxcomex.IFaxAccountIncomingQueue
title: IFaxAccountIncomingQueue
author: windows-sdk-content
description: Used by a fax client application to retrieve the inbound fax jobs (FaxIncomingJobs object) in the job queue for a particular fax account.
old-location: fax\_mfax_faxaccountincomingqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\faxinta_n_ifaxaccountincomingqueue_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxAccountIncomingQueue, IFaxAccountIncomingQueue interface [Fax Service], IFaxAccountIncomingQueue interface [Fax Service],described, _mfax_faxaccountincomingqueue_cpp, fax._mfax_faxaccountincomingqueue_cpp, faxcomex/IFaxAccountIncomingQueue
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFaxAccountIncomingQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountIncomingQueue interface


## -description


Used by a fax client application to retrieve the inbound fax jobs (<a href="https://msdn.microsoft.com/en-us/library/ms684959(v=VS.85).aspx">FaxIncomingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountIncomingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa359052(v=VS.85).aspx">IFaxAccountFolders</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxAccountIncomingQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Aa359044(v=VS.85).aspx">GetJob</a>
</td>
<td align="left" width="63%">
Returns an incoming fax job in the job queue of the current fax account according to the job's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359045(v=VS.85).aspx">GetJobs</a>
</td>
<td align="left" width="63%">
Returns the collection of inbound fax jobs in the queue for the current fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358954(v=VS.85).aspx">FaxAccountIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359052(v=VS.85).aspx">IFaxAccountFolders</a>
 

 

