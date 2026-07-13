---
UID: NN:icontact.IContact
title: IContact (icontact.h)
description: Do not use. Defines methods for reading and writing properties for a single contact.
helpviewer_keywords: ["IContact","IContact interface [Windows Contacts]","IContact interface [Windows Contacts]","described","_wincontacts_IContact","icontact/IContact","wincontacts._wincontacts_IContact"]
old-location: wincontacts\_wincontacts_IContact.htm
tech.root: wincontacts
ms.assetid: 9dc97b84-ede9-4ec1-939a-2b13e0d68486
ms.date: 12/05/2018
ms.keywords: IContact, IContact interface [Windows Contacts], IContact interface [Windows Contacts],described, _wincontacts_IContact, icontact/IContact, wincontacts._wincontacts_IContact
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContact
 - icontact/IContact
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
 - IContact
---

# IContact interface


## -description

Do not use. Defines methods for reading and writing properties for a single contact.

## -inheritance

The <b>IContact</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContact</b> also has these types of members:

## -remarks

Classes that implement this interface often also implement these interfaces:
            

<ul>
<li>
<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>: Enables the contact 
            to be loaded from a file. Use this interface when loading a contact to get full support 
            in <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontact-commitchanges">CommitChanges</a> to change conflict detection.</li>
<li>
<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>: Provides methods for saving and 
			loading objects that use a simple serial stream for their storage needs.</li>
<li>
<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>: Enables the contact to be saved 
			or loaded from a stream. Use <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">IPersistStreamInit::InitNew</a> to create a 
			new <b>IContact</b>. 
			Note: loading a contact with <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> does 
			not give you the locking and conflict detection that <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> 
			and <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontact-commitchanges">CommitChanges</a> do.</li>
<li>
<a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactproperties">IContactProperties</a>: Enables manipulation of contact properties.</li>
</ul>
