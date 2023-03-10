---
UID: NF:propsys.IPropertySystem.RegisterPropertySchema
title: IPropertySystem::RegisterPropertySchema (propsys.h)
description: Informs the schema subsystem of the addition of a property description schema file. (IPropertySystem.RegisterPropertySchema)
helpviewer_keywords: ["IPropertySystem interface [Windows Properties]","RegisterPropertySchema method","IPropertySystem.RegisterPropertySchema","IPropertySystem::RegisterPropertySchema","RegisterPropertySchema","RegisterPropertySchema method [Windows Properties]","RegisterPropertySchema method [Windows Properties]","IPropertySystem interface","properties.IPropertySystem_RegisterPropertySchema","propsys/IPropertySystem::RegisterPropertySchema","shell.IPropertySystem_RegisterPropertySchema","shell_IPropertySystem_RegisterPropertySchema"]
old-location: properties\IPropertySystem_RegisterPropertySchema.htm
tech.root: properties
ms.assetid: 752cc873-3fa8-4e05-97e7-41e90f059e4f
ms.date: 12/05/2018
ms.keywords: IPropertySystem interface [Windows Properties],RegisterPropertySchema method, IPropertySystem.RegisterPropertySchema, IPropertySystem::RegisterPropertySchema, RegisterPropertySchema, RegisterPropertySchema method [Windows Properties], RegisterPropertySchema method [Windows Properties],IPropertySystem interface, properties.IPropertySystem_RegisterPropertySchema, propsys/IPropertySystem::RegisterPropertySchema, shell.IPropertySystem_RegisterPropertySchema, shell_IPropertySystem_RegisterPropertySchema
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
 - IPropertySystem::RegisterPropertySchema
 - propsys/IPropertySystem::RegisterPropertySchema
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
 - IPropertySystem.RegisterPropertySchema
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

This method informs the schema subsystem of the addition of a property description schema (.propdesc) file, using a file path to the .propdesc file on the local computer. Call this method only when the file has first been installed on the computer. Typically, a setup application calls this method after installing the .propdesc file, which should be stored in the install directory of the application under "Program Files". Multiple calls may be made to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-registerpropertyschema">IPropertySystem::RegisterPropertySchema</a> in order to batch-register multiple schema files.

If a failure is encountered that prevents a property description from getting loaded, the cause will be recorded in the application event log. This method fails with E_ACCESSDENIED if the calling context does not have proper privileges, which include write access to HKLM (HKEY_LOCAL_MACHINE). It is the responsibility of the calling application to obtain privileges via limited user account (LUA) mechanisms.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>
