---
UID: NN:icontact.IContact
title: IContact
author: windows-sdk-content
description: Do not use. Defines methods for reading and writing properties for a single contact.
old-location: wincontacts\_wincontacts_IContact.htm
tech.root: wincontacts
ms.assetid: 9dc97b84-ede9-4ec1-939a-2b13e0d68486
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IContact, IContact interface [Windows Contacts], IContact interface [Windows Contacts],described, _wincontacts_IContact, icontact/IContact, wincontacts._wincontacts_IContact
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: icontact.h
req.include-header: Contact.h
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
 - IContact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContact interface


## -description


Do not use. Defines methods for reading and writing properties for a single contact. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContact</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContact</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContact</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b06f7d25-03ae-4630-9aa9-09cfbcecc416">CommitChanges</a>
</td>
<td align="left" width="63%">
Saves changes made to this contact to the contact file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25daa44f-2042-4116-b0dd-4f16857cbb0b">GetContactID</a>
</td>
<td align="left" width="63%">
Retrieves the local computer unique contact ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b037961-f2a4-4e75-a664-d70257bed426">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the file system path used to load this contact.

</td>
</tr>
</table> 


## -remarks



Classes that implement this interface often also implement these interfaces:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms687223(v=VS.85).aspx">IPersistFile</a>: Enables the contact 
            to be loaded from a file. Use this interface when loading a contact to get full support 
            in <a href="https://msdn.microsoft.com/b06f7d25-03ae-4630-9aa9-09cfbcecc416">CommitChanges</a> to change conflict detection.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms690091(v=VS.85).aspx">IPersistStream</a>: Provides methods for saving and 
			loading objects that use a simple serial stream for their storage needs.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms682273(v=VS.85).aspx">IPersistStreamInit</a>: Enables the contact to be saved 
			or loaded from a stream. Use <a href="https://msdn.microsoft.com/en-us/library/ms690234(v=VS.85).aspx">IPersistStreamInit::InitNew</a> to create a 
			new <b>IContact</b>. 
			Note: loading a contact with <a href="https://msdn.microsoft.com/en-us/library/ms690091(v=VS.85).aspx">IPersistStream</a> does 
			not give you the locking and conflict detection that <a href="https://msdn.microsoft.com/en-us/library/ms687284(v=VS.85).aspx">IPersistFile::Load</a> 
			and <a href="https://msdn.microsoft.com/b06f7d25-03ae-4630-9aa9-09cfbcecc416">CommitChanges</a> do.</li>
<li>
<a href="https://msdn.microsoft.com/c9c0d73d-4c39-4f7c-9bc6-46d764f157bd">IContactProperties</a>: Enables manipulation of contact properties.</li>
</ul>


