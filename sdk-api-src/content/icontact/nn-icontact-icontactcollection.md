---
UID: NN:icontact.IContactCollection
title: IContactCollection (icontact.h)
description: Do not use. Enumerates the contacts known by the IContactManager.
helpviewer_keywords: ["IContactCollection","IContactCollection interface [Windows Contacts]","IContactCollection interface [Windows Contacts]","described","_wincontacts_IContactCollection","icontact/IContactCollection","wincontacts._wincontacts_IContactCollection"]
old-location: wincontacts\_wincontacts_IContactCollection.htm
tech.root: wincontacts
ms.assetid: 4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897
ms.date: 12/05/2018
ms.keywords: IContactCollection, IContactCollection interface [Windows Contacts], IContactCollection interface [Windows Contacts],described, _wincontacts_IContactCollection, icontact/IContactCollection, wincontacts._wincontacts_IContactCollection
req.header: icontact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContactCollection
 - icontact/IContactCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactCollection
---

# IContactCollection interface


## -description

Do not use. Enumerates the contacts known by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactmanager">IContactManager</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContactCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContactCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Retrieves the current contact in the enumeration. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-next">Next</a>
</td>
<td align="left" width="63%">
Moves to the next contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to before the logical first element.

</td>
</tr>
</table>

## -remarks

This interface does not support deletion of contacts during an enumeration. Adding or removing contacts by other means during an enumeration results in undefined behavior. Modifying contact properties during enumeration is allowed.

