---
UID: NF:mergemod.IMsmDependency.get_Language
title: IMsmDependency::get_Language (mergemod.h)
description: The get_Language method retrieves the Language property of the Dependency object. This method returns the LANGID of the required module.
helpviewer_keywords: ["IMsmDependency interface","get_Language method","IMsmDependency.get_Language","IMsmDependency::get_Language","_msi_get_language_function_dependency_object_","get_Language","get_Language method","get_Language method","IMsmDependency interface","mergemod/IMsmDependency::get_Language","setup.imsmdependency_get_language"]
old-location: setup\imsmdependency_get_language.htm
tech.root: setup
ms.assetid: eb7e224d-948e-46d6-ac1b-cd851530cc8b
ms.date: 12/05/2018
ms.keywords: IMsmDependency interface,get_Language method, IMsmDependency.get_Language, IMsmDependency::get_Language, _msi_get_language_function_dependency_object_, get_Language, get_Language method, get_Language method,IMsmDependency interface, mergemod/IMsmDependency::get_Language, setup.imsmdependency_get_language
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
 - IMsmDependency::get_Language
 - mergemod/IMsmDependency::get_Language
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
 - IMsmDependency.get_Language
---

# IMsmDependency::get_Language


## -description

The 
<b>get_Language</b> method retrieves the 
<a href="/windows/desktop/Msi/dependency-language">Language</a> property of the 
<a href="/windows/desktop/Msi/dependency-object">Dependency</a> object. This method returns the <b>LANGID</b> of the required module.

## -parameters

### -param Language [out]

A pointer to a location in memory that receives the language.

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
Language is null.

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

## -see-also

<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmdependency">IMsmDependency</a>



<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>