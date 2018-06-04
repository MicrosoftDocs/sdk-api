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

# WSDXMLGetNameFromBuiltinNamespace function


## -description


Gets a specified name from the built-in namespace.


## -parameters




### -param pszNamespace

The namespace to match with a built-in namespace.


### -param pszName

The name to match with a built-in name.


### -param ppName

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that contains the returned built-in name.  The memory usage of <i>ppName</i> is managed elsewhere.  Consequently, the calling application should not attempt to deallocate <i>ppName</i>.


## -returns



This function can return one of these values.

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszNamespace</i> is <b>NULL</b>, <i>pszName</i> is <b>NULL</b>, the length in characters of <i>pszNamespace</i> exceeds WSD_MAX_TEXT_LENGTH (8192), the length in characters of <i>pszName</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or there was no matching name in the built-in namespace.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 



