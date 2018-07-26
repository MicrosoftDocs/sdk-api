---
UID: NN:faxcomex.IFaxRecipients
title: IFaxRecipients
author: windows-sdk-content
description: The IFaxRecipients interface defines a FaxRecipients messaging collection is used by a fax client application to manage the fax recipient objects (FaxRecipient) that represent the recipients of a single fax document.
old-location: fax\_mfax_faxrecipients_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7o4z_cpp.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFaxRecipients, IFaxRecipients interface [Fax Service], IFaxRecipients interface [Fax Service],described, _mfax_faxrecipients_cpp, fax._mfax_faxrecipients_cpp, faxcomex/IFaxRecipients
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
 - IFaxRecipients
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRecipients interface


## -description


The <b>IFaxRecipients</b> interface defines a <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> messaging collection is used by a fax client application to manage the fax recipient objects (<a href="https://msdn.microsoft.com/library/ms690204(v=VS.85).aspx">FaxRecipient</a>) that represent the recipients of a single fax document. The collection also includes methods to add and remove recipients. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxRecipients</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxRecipients</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxRecipients</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689572(v=VS.85).aspx">IFaxRecipients::Add</a> method adds a new <a href="https://msdn.microsoft.com/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object to the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms688373(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms688373(v=VS.85).aspx">IFaxRecipients::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> method returns a <a href="https://msdn.microsoft.com/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object from the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a3874a59-2eed-4cfb-b90e-2a437c00a5ae">IFaxRecipients::Remove</a> method removes an item from the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxRecipients</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms688447(v=VS.85).aspx">IFaxRecipients::get_Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. This is the total number of recipients associated with the fax server or fax document.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxRecipients</b> is provided as the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> object. 



