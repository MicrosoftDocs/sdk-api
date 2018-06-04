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

# SHGetAttributesFromDataObject function


## -description


<p class="CCE_Message">[<b>SHGetAttributesFromDataObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves specified pieces of information from a system data object.


## -parameters




### -param pdo [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

The data object from which to retrieve the information.


### -param dwAttributeMask

Type: <b>DWORD</b>

One or more of the <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO</a> flags that indicate which pieces of information the calling application wants to retrieve.


### -param pdwAttributes [out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that, when this function returns successfully, receives one or more <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO</a> flags that indicate the attributes, among those requested, that are common to all items in <i>pdo</i>. This pointer can be <b>NULL</b> if this information is not needed.


### -param pcItems [out, optional]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> that, when this function returns successfully, receives the number of PIDLs in the data object pointed to by <i>pdo</i>. This pointer can be <b>NULL</b> if this information is not needed.


## -returns



Type: <b>HRESULT</b>

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not a system data object. In this case, <i>pdwAttributes</i> is set to 0.

</td>
</tr>
</table>
 



