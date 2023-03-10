---
UID: NF:icontact.IContact.GetPath
title: IContact::GetPath (icontact.h)
description: Retrieves the file system path used to load this contact.
helpviewer_keywords: ["GetPath","GetPath method [Windows Contacts]","GetPath method [Windows Contacts]","IContact interface","IContact interface [Windows Contacts]","GetPath method","IContact.GetPath","IContact::GetPath","_wincontacts_IContact_GetPath","icontact/IContact::GetPath","wincontacts._wincontacts_IContact_GetPath"]
old-location: wincontacts\_wincontacts_IContact_GetPath.htm
tech.root: wincontacts
ms.assetid: 4b037961-f2a4-4e75-a664-d70257bed426
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [Windows Contacts], GetPath method [Windows Contacts],IContact interface, IContact interface [Windows Contacts],GetPath method, IContact.GetPath, IContact::GetPath, _wincontacts_IContact_GetPath, icontact/IContact::GetPath, wincontacts._wincontacts_IContact_GetPath
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
 - IContact::GetPath
 - icontact/IContact::GetPath
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
 - IContact.GetPath
---

# IContact::GetPath


## -description

Retrieves the file system path used to load this contact.

## -parameters

### -param pszPath [in, out]

Type: <b>LPWSTR</b>

User-allocated buffer to store the contact ID.

### -param cchPath [in]

Type: <b>DWORD</b>

Specifies the allocated buffer size in characters.

### -param pdwcchPathRequired [in, out]

Type: <b>DWORD*</b>

Upon failure due to insufficient buffer, contains the required size for <i>pszPath</i>.

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
Success. <i>pszPath</i> contains the path. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Contact ID was not loaded from a file path. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Macro HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) returned when <i>pszPath</i> was not large enough to store the value. The required buffer size is stored in <i>pdwcchPathRequired</i>. 

</td>
</tr>
</table>

