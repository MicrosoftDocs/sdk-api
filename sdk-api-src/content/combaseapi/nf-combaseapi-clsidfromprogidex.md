---
UID: NF:combaseapi.CLSIDFromProgIDEx
title: CLSIDFromProgIDEx function (combaseapi.h)
description: Triggers automatic installation if the COMClassStore policy is enabled.
helpviewer_keywords: ["CLSIDFromProgIDEx","CLSIDFromProgIDEx function [COM]","_com_CLSIDFromProgIDEx","com.clsidfromprogidex","combaseapi/CLSIDFromProgIDEx"]
old-location: com\clsidfromprogidex.htm
tech.root: com
ms.assetid: 2f937ac1-b214-482a-af4b-8cc8c0c585c3
ms.date: 12/05/2018
ms.keywords: CLSIDFromProgIDEx, CLSIDFromProgIDEx function [COM], _com_CLSIDFromProgIDEx, com.clsidfromprogidex, combaseapi/CLSIDFromProgIDEx
f1_keywords:
- combaseapi/CLSIDFromProgIDEx
dev_langs:
- c++
req.header: combaseapi.h
req.include-header: Objbase.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ole32.dll
api_name:
- CLSIDFromProgIDEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CLSIDFromProgIDEx function


## -description


Triggers automatic installation if the COMClassStore policy is enabled.

This is analogous to the behavior of <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> when neither CLSCTX_ENABLE_CODE_DOWNLOAD nor CLSCTX_NO_CODE_DOWNLOAD are specified.


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




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid">ProgIDFromCLSID</a>
 

 

