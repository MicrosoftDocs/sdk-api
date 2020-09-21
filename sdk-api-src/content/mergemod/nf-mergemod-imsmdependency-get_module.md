---
UID: NF:mergemod.IMsmDependency.get_Module
title: IMsmDependency::get_Module (mergemod.h)
description: The get_Module method retrieves the Module property of the Dependency object. This method returns the ModuleID of the module required by the current string in the form of a BSTR. The ModuleID is of the same form as used in the ModuleSignature table.
helpviewer_keywords: ["IMsmDependency interface","get_Module method","IMsmDependency.get_Module","IMsmDependency::get_Module","_msi_get_module_function","get_Module","get_Module method","get_Module method","IMsmDependency interface","mergemod/IMsmDependency::get_Module","setup.imsmdependency_get_module"]
old-location: setup\imsmdependency_get_module.htm
tech.root: setup
ms.assetid: 2a3e85ea-4727-45ca-a8c9-c168b9cb7467
ms.date: 12/05/2018
ms.keywords: IMsmDependency interface,get_Module method, IMsmDependency.get_Module, IMsmDependency::get_Module, _msi_get_module_function, get_Module, get_Module method, get_Module method,IMsmDependency interface, mergemod/IMsmDependency::get_Module, setup.imsmdependency_get_module
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
 - IMsmDependency::get_Module
 - mergemod/IMsmDependency::get_Module
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
 - IMsmDependency.get_Module
---

# IMsmDependency::get_Module


## -description

The 
<b>get_Module</b> method retrieves the 
<a href="/windows/desktop/Msi/dependency-module">Module</a> property of the 
<a href="/windows/desktop/Msi/dependency-object">Dependency</a> object. This method returns the ModuleID of the module required by the current string in the form of a <b>BSTR</b>. The ModuleID is of the same form as used in the 
<a href="/windows/desktop/Msi/modulesignature-table">ModuleSignature table</a>.

## -parameters

### -param Module [out]

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
Module is null

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded

</td>
</tr>
</table>

## -remarks

The client is responsible for freeing the resulting string using <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmdependency">IMsmDependency</a>



<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>