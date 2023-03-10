---
UID: NF:mergemod.IMsmDependency.get_Version
title: IMsmDependency::get_Version (mergemod.h)
description: The get_Version method retrieves the Version property of the Dependency object. This method returns the version of the required module in the form of a BSTR.
helpviewer_keywords: ["IMsmDependency interface","get_Version method","IMsmDependency.get_Version","IMsmDependency::get_Version","_msi_get_version_function","get_Version","get_Version method","get_Version method","IMsmDependency interface","mergemod/IMsmDependency::get_Version","setup.imsmdependency_get_version"]
old-location: setup\imsmdependency_get_version.htm
tech.root: setup
ms.assetid: 122542f9-b7b5-4e22-b05f-bd5dd04e5a2f
ms.date: 12/05/2018
ms.keywords: IMsmDependency interface,get_Version method, IMsmDependency.get_Version, IMsmDependency::get_Version, _msi_get_version_function, get_Version, get_Version method, get_Version method,IMsmDependency interface, mergemod/IMsmDependency::get_Version, setup.imsmdependency_get_version
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmDependency::get_Version
 - mergemod/IMsmDependency::get_Version
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmDependency.get_Version
---

# IMsmDependency::get_Version


## -description

The 
<b>get_Version</b> method retrieves the 
<a href="/windows/desktop/Msi/dependency-version">Version</a> property of the 
<a href="/windows/desktop/Msi/dependency-object">Dependency</a> object. This method returns the version of the required module in the form of a <b>BSTR</b>.

## -parameters

### -param Version [out]

A pointer to a location in memory that is filled in with a <b>BSTR</b> value.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Version is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

The client is responsible for freeing the resulting string using <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmdependency">IMsmDependency</a>



<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>