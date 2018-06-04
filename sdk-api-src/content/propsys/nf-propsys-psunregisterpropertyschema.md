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

# PSUnregisterPropertySchema function


## -description


Informs the schema subsystem of the removal of a property description schema file.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

Pointer to the full file path, as a Unicode string, to the property description schema (.propdesc) file on the local machine. This can be either a fully-specified full path, or a full path that includes environment variables such as <code>%PROGRAMFILES%</code>.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
The schema was unregistered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling context does not have proper privileges.

</td>
</tr>
</table>
 




## -remarks



This function is a wrapper for the schema subsystem's implementation of <a href="shell.IPropertySystem_UnregisterPropertySchema">IPropertySystem::UnregisterPropertySchema</a>. Call this method when the file is being uninstalled from the computer. Typically, a setup application calls this method before or after uninstalling the .propdesc file. This method can be called after the file no longer exists.

This function fails with a code of E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to HKLM (HKEY_LOCAL_MACHINE). It is the responsibility of the calling application to obtain privileges through User Account Control (UAC) mechanisms.




## -see-also




<a href="shell.PSRegisterPropertySchema">PSRegisterPropertySchema</a>
 

 

