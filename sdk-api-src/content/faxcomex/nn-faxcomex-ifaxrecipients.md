---
UID: NN:faxcomex.IFaxRecipients
title: IFaxRecipients (faxcomex.h)
description: The IFaxRecipients interface defines a FaxRecipients messaging collection is used by a fax client application to manage the fax recipient objects (FaxRecipient) that represent the recipients of a single fax document.
old-location: fax\_mfax_faxrecipients_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7o4z_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxRecipients, IFaxRecipients interface [Fax Service], IFaxRecipients interface [Fax Service],described, _mfax_faxrecipients_cpp, fax._mfax_faxrecipients_cpp, faxcomex/IFaxRecipients
ms.topic: interface
f1_keywords:
- faxcomex/IFaxRecipients
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
- IFaxRecipients
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxRecipients interface


## -description


The <b>IFaxRecipients</b> interface defines a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> messaging collection is used by a fax client application to manage the fax recipient objects (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a>) that represent the recipients of a single fax document. The collection also includes methods to add and remove recipients. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxRecipients</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxRecipients</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-add-vb">Add</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-add-vb">IFaxRecipients::Add</a> method adds a new <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a> object to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxrecipients-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxrecipients-get__newenum">IFaxRecipients::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxrecipients-get_item">Item</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-item">Item</a> method returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a> object from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-remove-vb">Remove</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-remove-vb">IFaxRecipients::Remove</a> method removes an item from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-count-vb">IFaxRecipients::get_Count</a> property represents the number of objects in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection. This is the total number of recipients associated with the fax server or fax document.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxRecipients</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> object. 



