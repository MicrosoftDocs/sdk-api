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

# IStreamBufferConfigure3::SetNamespace


## -description


The <b>SetNamespace</b> method specifies a prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.


## -parameters




### -param pszNamespace [in]

Pointer to a null-terminated wide character string. If <b>NULL</b>, no prefix is used. Currently, the following values are supported.

<ul>
<li>L"Global"</li>
<li><b>NULL</b></li>
</ul>

## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified prefix is not supported.

</td>
</tr>
</table>
 




## -remarks



The default value is "Global".

If the value is "Global", the synchronization objects are created in the global name space, which requires administrator privileges in Windows Vista or later. If the value is <b>NULL</b>, the synchronization objects are created in the local session name space, which does not require administrator privileges.




## -see-also




<a href="https://msdn.microsoft.com/73f3cd43-11d1-4eff-861d-087bfda7d135">IStreamBufferConfigure3 Interface</a>
 

 

