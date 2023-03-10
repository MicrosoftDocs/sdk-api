---
UID: NF:oleauto.RegisterTypeLib
title: RegisterTypeLib function (oleauto.h)
description: Adds information about a type library to the system registry.
helpviewer_keywords: ["RegisterTypeLib","RegisterTypeLib function [Automation]","_oa96_RegisterTypeLib","automat.registertypelib","oleauto/RegisterTypeLib"]
old-location: automat\registertypelib.htm
tech.root: automat
ms.assetid: d0559a57-b1a4-4036-97ed-024d775cb595
ms.date: 12/05/2018
ms.keywords: RegisterTypeLib, RegisterTypeLib function [Automation], _oa96_RegisterTypeLib, automat.registertypelib, oleauto/RegisterTypeLib
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterTypeLib
 - oleauto/RegisterTypeLib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - RegisterTypeLib
---

# RegisterTypeLib function


## -description

Adds information about a type library to the system registry.

## -parameters

### -param ptlib

The type library.

### -param szFullPath [in]

The fully qualified path specification for the type library.

### -param szHelpDir [in, optional]

The directory in which the Help file for the library being registered can be found. This parameter can be null.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR
</b></dt>
</dl>
</td>
<td width="60%">
The function could not write to the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_REGISTRYACCESS
</b></dt>
</dl>
</td>
<td width="60%">
The system registration database could not be opened.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE
</b></dt>
</dl>
</td>
<td width="60%">
The type library could not be opened.


</td>
</tr>
</table>

## -remarks

This function can be used during application initialization to register the application's type library correctly. When <b>RegisterTypeLib</b> is called to register a type library, both the minor and major version numbers are registered in hexadecimal.



In addition to filling in a complete registry entry under the type library key, <b>RegisterTypeLib</b> adds entries for each of the dispinterfaces and Automation-compatible interfaces, including dual interfaces. This information is required to create instances of these interfaces. Coclasses are not registered (that is, <b>RegisterTypeLib</b> does not write any values to the CLSID key of the coclass).

