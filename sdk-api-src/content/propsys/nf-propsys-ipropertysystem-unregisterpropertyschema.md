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

# IPropertySystem::UnregisterPropertySchema


## -description


Informs the schema subsystem of the removal of a property description schema (.propdesc) file, using a file path to the .propdesc file on the local machine.


## -parameters




### -param pszPath [in]

Type: <b>LPCWSTR</b>

Pointer to the file path for the .propdesc file on the local machine.


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
Indicates schema is unregistered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Indicates calling context does not have proper privileges.

</td>
</tr>
</table>
 




## -remarks



Call this method when the file is being uninstalled from the machine. Typically, a setup application calls this method before or after uninstalling the .propdesc file. This method can be called after the file no longer exists.

Call <a href="shell.IPropertySystem_RefreshPropertySchema">IPropertySystem::RefreshPropertySchema</a> in order for the newly-unregistered schema files to be unincorporated from the search index and the schema subsystem cache.

This method fails with E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to the local machine. It is the caller's responsibility to obtain privileges via least-privileged user account (LUA) mechanisms.




## -see-also




<a href="shell.IPropertySystem">IPropertySystem</a>
 

 

