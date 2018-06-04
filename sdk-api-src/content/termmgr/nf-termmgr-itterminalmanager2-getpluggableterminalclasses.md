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

# ITTerminalManager2::GetPluggableTerminalClasses


## -description


The 
<b>GetPluggableTerminalClasses</b> method lists the terminal classes for all pluggable terminals registered under a terminal superclass.


## -parameters




### -param iidSuperclass [in]

A <b>BSTR</b> that represents the CLSID for the parent superclass.


### -param dwMediaTypes [in]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a>. The method returns only terminals that support these media types.


### -param pdwNumClasses [in, out]

If the <i>pTerminalClasses</i> parameter is <b>NULL</b>, this parameter returns the total number of terminals registered under the terminal superclass specified by the <i>iidSuperclass</i> parameter. 




If <i>pTerminalClasses</i> is not <b>NULL</b>, and the method completes successfully, this parameter returns a count of the number of terminal IIDs returned in the <i>pTerminalClasses</i> buffer.


### -param pTerminalClasses [out]

Pointer to the buffer to receive the terminals IIDs. This parameter can also be <b>NULL</b>. For more information, see the description of the <i>pdwNumClasses</i> parameter.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminalClasses</i> parameter doesn't represent an IID or list of IIDs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminalClasses</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f91c8684-27f8-4db8-99ff-d5a6cb87a0c2">ITTerminalManager2</a>
 

 

