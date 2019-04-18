---
UID: NN:icontact.IContactCollection
title: IContactCollection (icontact.h)
author: windows-sdk-content
description: Do not use. Enumerates the contacts known by the IContactManager.
old-location: wincontacts\_wincontacts_IContactCollection.htm
tech.root: wincontacts
ms.assetid: 4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContactCollection, IContactCollection interface [Windows Contacts], IContactCollection interface [Windows Contacts],described, _wincontacts_IContactCollection, icontact/IContactCollection, wincontacts._wincontacts_IContactCollection
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContactCollection interface


## -description


Do not use. Enumerates the contacts known by the <a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContactCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e5a5d27d-121a-4755-892e-53d148facd74">GetCurrent</a>
</td>
<td align="left" width="63%">
Retrieves the current contact in the enumeration. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7d47643-4ef2-41fb-9f75-2fe79fec2385">Next</a>
</td>
<td align="left" width="63%">
Moves to the next contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31922d03-079e-4a6f-8516-d4cf540d812e">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to before the logical first element.

</td>
</tr>
</table> 


## -remarks



This interface does not support deletion of contacts during an enumeration. Adding or removing contacts by other means during an enumeration results in undefined behavior. Modifying contact properties during enumeration is allowed. 



