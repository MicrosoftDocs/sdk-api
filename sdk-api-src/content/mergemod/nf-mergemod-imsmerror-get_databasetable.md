---
UID: NF:mergemod.IMsmError.get_DatabaseTable
title: IMsmError::get_DatabaseTable (mergemod.h)
description: The get_DatabaseTable method retrieves the DatabaseTable property of the Error object. The method returns the name of the table in the database that caused the error.
helpviewer_keywords: ["IMsmError interface","get_DatabaseTable method","IMsmError.get_DatabaseTable","IMsmError::get_DatabaseTable","_msi_get_databasetable_function","get_DatabaseTable","get_DatabaseTable method","get_DatabaseTable method","IMsmError interface","mergemod/IMsmError::get_DatabaseTable","setup.imsmerror_get_databasetable"]
old-location: setup\imsmerror_get_databasetable.htm
tech.root: setup
ms.assetid: fee774b3-66ee-4ffd-b000-8032118e9a9d
ms.date: 12/05/2018
ms.keywords: IMsmError interface,get_DatabaseTable method, IMsmError.get_DatabaseTable, IMsmError::get_DatabaseTable, _msi_get_databasetable_function, get_DatabaseTable, get_DatabaseTable method, get_DatabaseTable method,IMsmError interface, mergemod/IMsmError::get_DatabaseTable, setup.imsmerror_get_databasetable
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
 - IMsmError::get_DatabaseTable
 - mergemod/IMsmError::get_DatabaseTable
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
 - IMsmError.get_DatabaseTable
---

# IMsmError::get_DatabaseTable


## -description

The 
<b>get_DatabaseTable</b> method retrieves the 
<a href="/windows/desktop/Msi/error-databasetable">DatabaseTable</a> property of the 
<a href="/windows/desktop/Msi/error-object">Error</a> object. The method returns the name of the table in the database that caused the error.

## -parameters

### -param ErrorTable [out]

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
Table is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system was unable to allocate memory for the string.

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

The collection is empty if the values do not apply to the type of the error. You can determine the type of error by calling <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmerror-get_type">IMsmError::get_Type</a>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>