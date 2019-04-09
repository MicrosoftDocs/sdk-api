---
UID: NF:icontact.IContactManager.Load
title: IContactManager::Load (icontact.h)
author: windows-sdk-content
description: Loads an IContact object with the data from the contact referenced by the computer-local contact ID.
old-location: wincontacts\_wincontacts_IContactManager_Load.htm
tech.root: wincontacts
ms.assetid: d9addc49-72fd-4b87-bf48-a2a09b1161e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContactManager interface [Windows Contacts],Load method, IContactManager.Load, IContactManager::Load, Load, Load method [Windows Contacts], Load method [Windows Contacts],IContactManager interface, _wincontacts_IContactManager_Load, icontact/IContactManager::Load, wincontacts._wincontacts_IContactManager_Load
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
 - IContactManager.Load
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactManager::Load


## -description


Loads an <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a> object with the data from the contact 
		referenced by the computer-local contact ID.


## -parameters




### -param pszContactID [in]

Type: <b>LPCWSTR</b>

Specifies the contact ID to load.


### -param ppContact [out]

Type: <b><a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>**</b>

Specifies the destination <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a> object.


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
Contact was found and loaded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Could not find this contact ID. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/25daa44f-2042-4116-b0dd-4f16857cbb0b">GetContactID</a>



<a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a>
 

 

