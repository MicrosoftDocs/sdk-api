---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IContactProperties::SetBinary


## -description


Sets the binary data at a specified property to the contents of a specified <a href="_stg_istream">IStream interface [Structured Storage]</a>, 
		which contains a null-terminated string (as MIME type) data. 


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to set.


### -param dwFlags [in]

Type: <b>DWORD</b>

CGD_DEFAULT can be used to create or overwrite the value at <i>pszPropertyName</i>. 


### -param pszContentType [in]

Type: <b>LPWSTR</b>

Specifies null-terminated string representing MIME type to store when CGD_DEFAULT. 


### -param pStream [in]

Type: <b>IStream*</b>

Pointer to <a href="_stg_istream">IStream interface [Structured Storage]</a> object containing data to place at this node. 
				NOTE: IStream::Read is called for the data until it succeeds with a zero-length read. 
				Any other return value results in a failure and no change. 


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
Value is set successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Property name is invalid for set, or property name doesn't exist for delete. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Unable to set the value for this property due to schema. 

</td>
</tr>
</table>
 




## -remarks



To set a single-level property, set <i>pszPropertyName</i> to the property name. 

To set a property from a multi-value property, set <i>pszPropertyName</i> 
		to the form: toplevel/secondlevel[4]/thirdlevel.



