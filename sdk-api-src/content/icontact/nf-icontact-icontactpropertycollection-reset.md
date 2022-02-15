---
UID: NF:icontact.IContactPropertyCollection.Reset
title: IContactPropertyCollection::Reset (icontact.h)
description: Resets enumeration of properties.
helpviewer_keywords: ["IContactPropertyCollection interface [Windows Contacts]","Reset method","IContactPropertyCollection.Reset","IContactPropertyCollection::Reset","Reset","Reset method [Windows Contacts]","Reset method [Windows Contacts]","IContactPropertyCollection interface","_wincontacts_IContactPropertyCollection_Reset","icontact/IContactPropertyCollection::Reset","wincontacts._wincontacts_IContactPropertyCollection_Reset"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection_Reset.htm
tech.root: wincontacts
ms.assetid: cef73e3c-56be-44b8-b05b-3c2081b71591
ms.date: 12/05/2018
ms.keywords: IContactPropertyCollection interface [Windows Contacts],Reset method, IContactPropertyCollection.Reset, IContactPropertyCollection::Reset, Reset, Reset method [Windows Contacts], Reset method [Windows Contacts],IContactPropertyCollection interface, _wincontacts_IContactPropertyCollection_Reset, icontact/IContactPropertyCollection::Reset, wincontacts._wincontacts_IContactPropertyCollection_Reset
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
 - IContactPropertyCollection::Reset
 - icontact/IContactPropertyCollection::Reset
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
 - IContactPropertyCollection.Reset
---

# IContactPropertyCollection::Reset


## -description

Resets enumeration of properties.



## -returns

Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Reset is successful. 

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Collection has been reset to the location before the first element (if any elements are present), 
		so you must call <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactpropertycollection-next">IContactPropertyCollection::Next</a> to begin querying data.</div>
<div> </div>
