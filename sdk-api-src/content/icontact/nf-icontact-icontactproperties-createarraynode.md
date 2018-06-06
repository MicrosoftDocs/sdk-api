---
UID: NF:icontact.IContactProperties.CreateArrayNode
title: IContactProperties::CreateArrayNode
author: windows-sdk-content
description: Creates a new array node in a multi-value property.
old-location: wincontacts\_wincontacts_IContactProperties_CreateArrayNode.htm
old-project: wincontacts
ms.assetid: 422b9991-c8ac-4e8b-9432-1ccba02f7cfd
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: CreateArrayNode, CreateArrayNode method [Windows Contacts], CreateArrayNode method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],CreateArrayNode method, IContactProperties.CreateArrayNode, IContactProperties::CreateArrayNode, _wincontacts_IContactProperties_CreateArrayNode, icontact/IContactProperties::CreateArrayNode, wincontacts._wincontacts_IContactProperties_CreateArrayNode
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
 - IContactProperties.CreateArrayNode
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactProperties::CreateArrayNode


## -description


Creates a new array node in a multi-value property.


## -parameters




### -param pszArrayName [in]

Type: <b>LPCWSTR</b>

Specifies the top-level property for which to create a new node.


### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT. 


### -param fAppend [in]

Type: <b>BOOL</b>

TRUE for insert after, <b>FALSE</b> for insert before. 


### -param pszNewArrayElementName [in, out]

Type: <b>LPWSTR</b>

Specifies a user-allocated buffer to store the new array element name. 


### -param cchNewArrayElementName [in]

Type: <b>DWORD</b>

Specifies an allocated buffer size in characters. 


### -param pdwcchNewArrayElementNameRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszNewArrayElementName</i>. 


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
New node is created and name is in <i>pszNewArrayElementName</i>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Macro HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) returned when array name is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Macro HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) returned when <i>pszNewArrayElementName</i> 

					is not large enough to store the value. The required buffer size is stored in 
					<i>pdwcchNewArrayElementNameRequired</i>. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  The first element of an existing set is at index 1. </div>
<div> </div>
To create a <i>pszArrayName</i> at toplevel/secondlevel[1], 
		call this function with <i>pszArrayName</i> == toplevel, fAppend=<b>FALSE</b>. 

To create an array node that is an extension at [namespace]toplevel/secondlevel[1], 
		call this function with <i>pszArrayName</i> == [namespace:secondlevel]toplevel. 

To append to the set, pass <i>fAppend</i>=TRUE instead; 
		<i>pszNewArrayElementName</i> then contains the resulting array node name, including the index.



