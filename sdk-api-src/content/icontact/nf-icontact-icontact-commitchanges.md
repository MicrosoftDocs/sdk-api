---
UID: NF:icontact.IContact.CommitChanges
title: IContact::CommitChanges
author: windows-sdk-content
description: Saves changes made to this contact to the contact file.
old-location: wincontacts\_wincontacts_IContact_CommitChanges.htm
old-project: wincontacts
ms.assetid: b06f7d25-03ae-4630-9aa9-09cfbcecc416
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: CommitChanges, CommitChanges method [Windows Contacts], CommitChanges method [Windows Contacts],IContact interface, IContact interface [Windows Contacts],CommitChanges method, IContact.CommitChanges, IContact::CommitChanges, _wincontacts_IContact_CommitChanges, icontact/IContact::CommitChanges, wincontacts._wincontacts_IContact_CommitChanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContact.CommitChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
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



