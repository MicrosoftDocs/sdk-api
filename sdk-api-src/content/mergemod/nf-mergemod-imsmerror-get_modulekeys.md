---
UID: NF:mergemod.IMsmError.get_ModuleKeys
title: IMsmError::get_ModuleKeys (mergemod.h)
description: The get_ModuleKeys method retrieves the ModuleKeys property of the Error object. This method returns a pointer to a string collection that contains the primary keys of the row in the module causing the error, one key per entry in the collection.
helpviewer_keywords: ["IMsmError interface","get_ModuleKeys method","IMsmError.get_ModuleKeys","IMsmError::get_ModuleKeys","_msi_get_modulekeys_function","get_ModuleKeys","get_ModuleKeys method","get_ModuleKeys method","IMsmError interface","mergemod/IMsmError::get_ModuleKeys","setup.imsmerror_get_modulekeys"]
old-location: setup\imsmerror_get_modulekeys.htm
tech.root: setup
ms.assetid: f2f483c7-8d38-416e-af92-fd7ab6aef459
ms.date: 12/05/2018
ms.keywords: IMsmError interface,get_ModuleKeys method, IMsmError.get_ModuleKeys, IMsmError::get_ModuleKeys, _msi_get_modulekeys_function, get_ModuleKeys, get_ModuleKeys method, get_ModuleKeys method,IMsmError interface, mergemod/IMsmError::get_ModuleKeys, setup.imsmerror_get_modulekeys
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
 - IMsmError::get_ModuleKeys
 - mergemod/IMsmError::get_ModuleKeys
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
 - IMsmError.get_ModuleKeys
---

# IMsmError::get_ModuleKeys


## -description

The 
<b>get_ModuleKeys</b> method retrieves the 
<a href="/windows/desktop/Msi/error-modulekeys">ModuleKeys</a> property of the <a href="/windows/desktop/Msi/error-object">Error</a> object. This method returns a pointer to a string collection that contains the primary keys of the row in the module causing the error, one key per entry in the collection.

## -parameters

### -param ErrorKeys [out]

A pointer to a location in memory that receives a pointer to a string collection.

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
ErrorKeys is null.

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

The client is responsible for releasing the string collection when it is no longer required.

The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmerror-get_type">IMsmError::get_Type</a>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>