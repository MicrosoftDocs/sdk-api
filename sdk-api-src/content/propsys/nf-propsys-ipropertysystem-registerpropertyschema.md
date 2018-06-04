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

# IPropertySystem::RegisterPropertySchema


## -description


Informs the schema subsystem of the addition of a property description schema file.


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
Indicates schema is registered.

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
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
Indicates one or more of the property descriptions in the schema was not registered.

</td>
</tr>
</table>
 




## -remarks



This method informs the schema subsystem of the addition of a property description schema (.propdesc) file, using a file path to the .propdesc file on the local computer. Call this method only when the file has first been installed on the computer. Typically, a setup application calls this method after installing the .propdesc file, which should be stored in the install directory of the application under "Program Files". Multiple calls may be made to <a href="shell.IPropertySystem_RegisterPropertySchema">IPropertySystem::RegisterPropertySchema</a> in order to batch-register multiple schema files.

If a failure is encountered that prevents a property description from getting loaded, the cause will be recorded in the application event log. This method fails with E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to HKLM (HKEY_LOCAL_MACHINE). It is the responsibility of the calling application to obtain privileges via limited user account (LUA) mechanisms.




## -see-also




<a href="shell.IPropertySystem">IPropertySystem</a>
 

 

