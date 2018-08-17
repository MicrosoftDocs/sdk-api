---
UID: NF:combaseapi.CLSIDFromProgIDEx
title: CLSIDFromProgIDEx function
author: windows-sdk-content
description: Triggers automatic installation if the COMClassStore policy is enabled.
old-location: com\clsidfromprogidex.htm
old-project: com
ms.assetid: 2f937ac1-b214-482a-af4b-8cc8c0c585c3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLSIDFromProgIDEx, CLSIDFromProgIDEx function [COM], _com_CLSIDFromProgIDEx, com.clsidfromprogidex, combaseapi/CLSIDFromProgIDEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CLSIDFromProgIDEx
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CLSIDFromProgIDEx function


## -description


Triggers automatic installation if the COMClassStore policy is enabled.

This is analogous to the behavior of <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> when neither CLSCTX_ENABLE_CODE_DOWNLOAD nor CLSCTX_NO_CODE_DOWNLOAD are specified.


## -parameters




### -param lpszProgID [in]

A pointer to the ProgID whose CLSID is requested.


### -param lpclsid [out]

Receives a pointer to the retrieved CLSID on return.


## -returns



This function can return the following values.

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
The CLSID was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
The registered CLSID for the ProgID is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_WRITEREGDB</b></dt>
</dl>
</td>
<td width="60%">
An error occurred writing the CLSID to the registry. See Remarks below.


</td>
</tr>
</table>
 




## -remarks



CLSCTX_ENABLE_CODE_DOWNLOAD enables automatic installation of missing classes through IntelliMirror/Application Management from the Active Directory. If this flag is not specified, the COMClassStore Policy ("Download missing COM components") determines the behavior (default: no download).



If the COMClassStore Policy enables automatic installation, CLSCTX_NO_CODE_DOWNLOAD can be used to explicitly disallow download for an activation.



If either of the following registry values are enabled (meaning set to 1), automatic download of missing classes is enabled:

<ul>
<li><b>HKEY_CURRENT_USER\Software\Policies\Microsoft\Windows\App Management</b>\<b>COMClassStore</b></li>
<li><b>HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\App Management
</b>\<b>COMClassStore</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690567(v=VS.85).aspx">ProgIDFromCLSID</a>
 

 

