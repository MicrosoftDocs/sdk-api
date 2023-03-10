---
UID: NF:icontact.IContactCollection.Next
title: IContactCollection::Next (icontact.h)
description: Moves to the next contact.
helpviewer_keywords: ["IContactCollection interface [Windows Contacts]","Next method","IContactCollection.Next","IContactCollection::Next","Next","Next method [Windows Contacts]","Next method [Windows Contacts]","IContactCollection interface","_wincontacts_IContactCollection_Next","icontact/IContactCollection::Next","wincontacts._wincontacts_IContactCollection_Next"]
old-location: wincontacts\_wincontacts_IContactCollection_Next.htm
tech.root: wincontacts
ms.assetid: f7d47643-4ef2-41fb-9f75-2fe79fec2385
ms.date: 12/05/2018
ms.keywords: IContactCollection interface [Windows Contacts],Next method, IContactCollection.Next, IContactCollection::Next, Next, Next method [Windows Contacts], Next method [Windows Contacts],IContactCollection interface, _wincontacts_IContactCollection_Next, icontact/IContactCollection::Next, wincontacts._wincontacts_IContactCollection_Next
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
 - IContactCollection::Next
 - icontact/IContactCollection::Next
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
 - IContactCollection.Next
---

# IContactCollection::Next


## -description

Moves to the next contact.



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
Move is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not move, positioned at the end of the collection. 

</td>
</tr>
</table>

## -remarks

After S_FALSE is returned, calls to GetCurrent will fail.

