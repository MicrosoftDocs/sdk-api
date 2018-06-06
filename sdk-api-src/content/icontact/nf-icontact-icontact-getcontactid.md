---
UID: NF:icontact.IContact.GetContactID
title: IContact::GetContactID
author: windows-sdk-content
description: Retrieves the local computer unique contact ID.
old-location: wincontacts\_wincontacts_IContact_GetContactID.htm
old-project: wincontacts
ms.assetid: 25daa44f-2042-4116-b0dd-4f16857cbb0b
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GetContactID, GetContactID method [Windows Contacts], GetContactID method [Windows Contacts],IContact interface, IContact interface [Windows Contacts],GetContactID method, IContact.GetContactID, IContact::GetContactID, _wincontacts_IContact_GetContactID, icontact/IContact::GetContactID, wincontacts._wincontacts_IContact_GetContactID
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
 - IContact.GetContactID
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContact::GetContactID


## -description


Retrieves the local computer unique contact ID.


## -parameters




### -param pszContactID [in, out]

Type: <b>LPWSTR</b>

User allocated buffer to store the contact ID.


### -param cchContactID [in]

Type: <b>DWORD</b>

Specifies allocated buffer size. 


### -param pdwcchContactIDRequired [in, out]

Type: <b>DWORD*</b>

Upon failure due to insufficient buffer, contains the required size for <i>pszContactID</i>. May be <b>NULL</b>. 


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
Success. <i>pszContactID</i> contains a null-terminated ContactID. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Macro HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) returned when <i>pszContactID</i> was not large enough to store the value. The required buffer size is stored in <i>pdwcchContactIDRequired</i>. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>



<a href="https://msdn.microsoft.com/d9addc49-72fd-4b87-bf48-a2a09b1161e9">Load</a>
 

 

