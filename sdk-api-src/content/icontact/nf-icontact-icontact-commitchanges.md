---
UID: NF:icontact.IContact.CommitChanges
title: IContact::CommitChanges (icontact.h)
description: Saves changes made to this contact to the contact file.
helpviewer_keywords: ["CommitChanges","CommitChanges method [Windows Contacts]","CommitChanges method [Windows Contacts]","IContact interface","IContact interface [Windows Contacts]","CommitChanges method","IContact.CommitChanges","IContact::CommitChanges","_wincontacts_IContact_CommitChanges","icontact/IContact::CommitChanges","wincontacts._wincontacts_IContact_CommitChanges"]
old-location: wincontacts\_wincontacts_IContact_CommitChanges.htm
tech.root: wincontacts
ms.assetid: b06f7d25-03ae-4630-9aa9-09cfbcecc416
ms.date: 12/05/2018
ms.keywords: CommitChanges, CommitChanges method [Windows Contacts], CommitChanges method [Windows Contacts],IContact interface, IContact interface [Windows Contacts],CommitChanges method, IContact.CommitChanges, IContact::CommitChanges, _wincontacts_IContact_CommitChanges, icontact/IContact::CommitChanges, wincontacts._wincontacts_IContact_CommitChanges
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
 - IContact::CommitChanges
 - icontact/IContact::CommitChanges
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
 - IContact.CommitChanges
---

# IContact::CommitChanges


## -description

Saves changes made to this contact to the contact file.

## -parameters

### -param dwCommitFlags [in]

Type: <b>DWORD</b>

Reserved parameter. Must be 0.

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
Changes written to disk successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Contact not loaded from a file path. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
Another process modified the file in a way incompatible with 
					changes to this contact. 

</td>
</tr>
</table>

## -remarks

If the contact changes between creation and <b>IContact::CommitChanges</b> 
		and an incompatible change was made on disk, may return ERROR_SHARING_VIOLATION.

