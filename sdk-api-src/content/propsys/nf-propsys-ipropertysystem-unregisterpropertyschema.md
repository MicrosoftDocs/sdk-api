---
UID: NF:propsys.IPropertySystem.UnregisterPropertySchema
title: IPropertySystem::UnregisterPropertySchema (propsys.h)
description: Informs the schema subsystem of the removal of a property description schema (.propdesc) file, using a file path to the .propdesc file on the local machine.
helpviewer_keywords: ["IPropertySystem interface [Windows Properties]","UnregisterPropertySchema method","IPropertySystem.UnregisterPropertySchema","IPropertySystem::UnregisterPropertySchema","UnregisterPropertySchema","UnregisterPropertySchema method [Windows Properties]","UnregisterPropertySchema method [Windows Properties]","IPropertySystem interface","properties.IPropertySystem_UnregisterPropertySchema","propsys/IPropertySystem::UnregisterPropertySchema","shell.IPropertySystem_UnregisterPropertySchema","shell_IPropertySystem_UnregisterPropertySchema"]
old-location: properties\IPropertySystem_UnregisterPropertySchema.htm
tech.root: properties
ms.assetid: de81e174-9c32-455f-a7ba-a3d1b2223b84
ms.date: 12/05/2018
ms.keywords: IPropertySystem interface [Windows Properties],UnregisterPropertySchema method, IPropertySystem.UnregisterPropertySchema, IPropertySystem::UnregisterPropertySchema, UnregisterPropertySchema, UnregisterPropertySchema method [Windows Properties], UnregisterPropertySchema method [Windows Properties],IPropertySystem interface, properties.IPropertySystem_UnregisterPropertySchema, propsys/IPropertySystem::UnregisterPropertySchema, shell.IPropertySystem_UnregisterPropertySchema, shell_IPropertySystem_UnregisterPropertySchema
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem::UnregisterPropertySchema
 - propsys/IPropertySystem::UnregisterPropertySchema
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPropertySystem.UnregisterPropertySchema
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

Call <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-refreshpropertyschema">IPropertySystem::RefreshPropertySchema</a> in order for the newly-unregistered schema files to be unincorporated from the search index and the schema subsystem cache.

This method fails with E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to the local machine. It is the caller's responsibility to obtain privileges via least-privileged user account (LUA) mechanisms.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>