---
UID: NF:propsys.PSRegisterPropertySchema
title: PSRegisterPropertySchema function (propsys.h)
description: Informs the schema subsystem of the addition of a property description schema file. (PSRegisterPropertySchema)
helpviewer_keywords: ["PSRegisterPropertySchema","PSRegisterPropertySchema function [Windows Properties]","properties.PSRegisterPropertySchema","propsys/PSRegisterPropertySchema","shell.PSRegisterPropertySchema","shell_PSRegisterPropertySchema"]
old-location: properties\PSRegisterPropertySchema.htm
tech.root: properties
ms.assetid: ea9c4361-fada-4b07-b450-dd0c6409745a
ms.date: 12/05/2018
ms.keywords: PSRegisterPropertySchema, PSRegisterPropertySchema function [Windows Properties], properties.PSRegisterPropertySchema, propsys/PSRegisterPropertySchema, shell.PSRegisterPropertySchema, shell_PSRegisterPropertySchema
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSRegisterPropertySchema
 - propsys/PSRegisterPropertySchema
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSRegisterPropertySchema
---

# PSRegisterPropertySchema function


## -description

Informs the schema subsystem of the addition of a property description schema file.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

Pointer to the full file path, as a Unicode string, to the <a href="/windows/desktop/properties/propdesc-schema-entry">property description schema</a> (.propdesc) file on the local machine. This can be either a fully-specified full path, or a full path that includes environment variables such as <code>%PROGRAMFILES%</code>.

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
All property descriptions in the schema were registered.

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
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
One or more property descriptions in the schema failed to register. The specific failures are logged in the application event log.

</td>
</tr>
</table>

## -remarks

This function is a wrapper API for the schema subsystem's implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-registerpropertyschema">IPropertySystem::RegisterPropertySchema</a>. Call this function only when the file is first installed on the computer. Typically, a setup application calls this function after it installs the .propdesc file, which should be stored in the install directory of the application under Program Files. Multiple calls can be made to <b>IPropertySystem::RegisterPropertySchema</b> in order to register multiple schema files.

When registering property schema files, remember that they can be read by processes running as different users. Therefore, it is important to place a schema file in a location that grants read access to all users on the machine. Similarly, use the absolute path to the file in this function's <i>pszPath</i> parameter.

<div class="alert"><b>Note</b>  Because schemas are specific to the machine and cannot be registered for each individual user, registering a file path under user profiles is not supported on Windows Vista.</div>
<div> </div>
If a full or partial failure is encountered that prevents a property description from being loaded, the cause is recorded in the application event log. This function fails with E_ACCESSDENIED if the calling context does not have proper privileges, which includes write access to HKEY_LOCAL_MACHINE. It is the responsibility of the calling application to obtain privileges through User Account Control (UAC) mechanisms.
