---
UID: NN:faxcomex._IFaxAccountNotify
title: "_IFaxAccountNotify"
author: windows-sdk-content
description: Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives.
old-location: fax\_mfax_ifaxaccountnotify.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\faxinto_z_ifaxaccountnotify.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxAccountNotify, IFaxAccountNotify interface [Fax Service], IFaxAccountNotify interface [Fax Service],described, IIFaxAccountNotify, _IFaxAccountNotify, _mfax_ifaxaccountnotify, fax._mfax_ifaxaccountnotify, faxcomex/_IFaxAccountNotify
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
 - IFaxAccountNotify
 - IIFaxAccountNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxAccountNotify interface


## -description


Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>_IFaxAccountNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxAccountNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359032(v=VS.85).aspx">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming fax job is added to the job queue for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359033(v=VS.85).aspx">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the status of an incoming fax job for a particular fax account changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359034(v=VS.85).aspx">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming fax job is removed from the job queue of a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359035(v=VS.85).aspx">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359036(v=VS.85).aspx">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359037(v=VS.85).aspx">OnOngoingMessageRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing message is removed from the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359038(v=VS.85).aspx">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing fax job is added to the job queue for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359039(v=VS.85).aspx">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the status of an outgoing fax job for a particular fax account changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359040(v=VS.85).aspx">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing fax job is removed from the job queue of a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359041(v=VS.85).aspx">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa359041(v=VS.85).aspx">IFaxAccountNotify::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359042(v=VS.85).aspx">OnServerShutDown</a>
</td>
<td align="left" width="63%">
Called by the fax service when it shuts down. 

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the <a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a> object:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Dim WithEvents objFaxAccount As FaxAccount
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxAccountNotify</b> and pass the fax service the pointer to an <b>IFaxAccountNotify</b> interface.
            



