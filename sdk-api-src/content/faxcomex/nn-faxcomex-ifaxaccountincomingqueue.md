---
UID: NN:faxcomex.IFaxAccountIncomingQueue
title: IFaxAccountIncomingQueue
author: windows-sdk-content
description: Used by a fax client application to retrieve the inbound fax jobs (FaxIncomingJobs object) in the job queue for a particular fax account.
old-location: fax\_mfax_faxaccountincomingqueue_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\faxinta_n_ifaxaccountincomingqueue_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxAccountIncomingQueue, IFaxAccountIncomingQueue interface [Fax Service], IFaxAccountIncomingQueue interface [Fax Service],described, _mfax_faxaccountincomingqueue_cpp, fax._mfax_faxaccountincomingqueue_cpp, faxcomex/IFaxAccountIncomingQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
 - IFaxAccountIncomingQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccountIncomingQueue interface


## -description


Used by a fax client application to retrieve the inbound fax jobs (<a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> object) in the job queue for a particular fax account.

The <b>IFaxAccountIncomingQueue</b> interface is accessed through the <a href="https://msdn.microsoft.com/f7a60c42-55c8-43c1-acce-3b4f36a1d219">IFaxAccountFolders</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingQueue</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxAccountIncomingQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/914601de-c370-4b22-891b-dfd205fe0c70">GetJob</a>
</td>
<td align="left" width="63%">
Returns an incoming fax job in the job queue of the current fax account according to the job's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcb21dfc-4131-4a91-9343-11052b567781">GetJobs</a>
</td>
<td align="left" width="63%">
Returns the collection of inbound fax jobs in the queue for the current fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dd0ba850-d2d0-4ba3-a36c-a0947ab44c28">FaxAccountIncomingQueue</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/f7a60c42-55c8-43c1-acce-3b4f36a1d219">IFaxAccountFolders</a>
 

 

