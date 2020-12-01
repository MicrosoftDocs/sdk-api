---
UID: NF:propsys.PSUnregisterPropertySchema
title: PSUnregisterPropertySchema function (propsys.h)
description: Informs the schema subsystem of the removal of a property description schema file.
helpviewer_keywords: ["PSUnregisterPropertySchema","PSUnregisterPropertySchema function [Windows Properties]","properties.PSUnregisterPropertySchema","propsys/PSUnregisterPropertySchema","shell.PSUnregisterPropertySchema","shell_PSUnregisterPropertySchema"]
old-location: properties\PSUnregisterPropertySchema.htm
tech.root: properties
ms.assetid: 57df82a9-8954-4c2b-b794-82ac542149e2
ms.date: 12/05/2018
ms.keywords: PSUnregisterPropertySchema, PSUnregisterPropertySchema function [Windows Properties], properties.PSUnregisterPropertySchema, propsys/PSUnregisterPropertySchema, shell.PSUnregisterPropertySchema, shell_PSUnregisterPropertySchema
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
 - PSUnregisterPropertySchema
 - propsys/PSUnregisterPropertySchema
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
 - PSUnregisterPropertySchema
---

# PSUnregisterPropertySchema function


## -description

Informs the schema subsystem of the removal of a property description schema file.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

Pointer to the full file path, as a Unicode string, to the property description schema (.propdesc) file on the local machine. This can be either a fully-specified full path, or a full path that includes environment variables such as <code>%PROGRAMFILES%</code>.

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
The schema was unregistered.

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
</table>

## -remarks

This function is a wrapper for the schema subsystem's implementation of <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-unregisterpropertyschema">IPropertySystem::UnregisterPropertySchema</a>. Call this method when the file is being uninstalled from the computer. Typically, a setup application calls this method before or after uninstalling the .propdesc file. This method can be called after the file no longer exists.

This function fails with a code of E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to HKLM (HKEY_LOCAL_MACHINE). It is the responsibility of the calling application to obtain privileges through User Account Control (UAC) mechanisms.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psregisterpropertyschema">PSRegisterPropertySchema</a>