---
UID: NF:evalcom2.IValidate.OpenDatabase
title: IValidate::OpenDatabase (evalcom2.h)
description: The OpenDatabase method opens a Windows Installer installation package or merge module for validation.
helpviewer_keywords: ["IValidate interface","OpenDatabase method","IValidate.OpenDatabase","IValidate::OpenDatabase","OpenDatabase","OpenDatabase method","OpenDatabase method","IValidate interface","evalcom2/IValidate::OpenDatabase","setup.ivalidate_opendatabase"]
old-location: setup\ivalidate_opendatabase.htm
tech.root: setup
ms.assetid: 3f295eea-5f6b-4afa-b0ac-55606086b2b2
ms.date: 12/05/2018
ms.keywords: IValidate interface,OpenDatabase method, IValidate.OpenDatabase, IValidate::OpenDatabase, OpenDatabase, OpenDatabase method, OpenDatabase method,IValidate interface, evalcom2/IValidate::OpenDatabase, setup.ivalidate_opendatabase
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
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
req.dll: Evalcom2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValidate::OpenDatabase
 - evalcom2/IValidate::OpenDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Evalcom2.dll
api_name:
 - IValidate.OpenDatabase
---

# IValidate::OpenDatabase


## -description

The <b>OpenDatabase</b> method opens a Windows Installer installation package or merge module for validation.

## -parameters

### -param szDatabase [in]

The fully qualified path to the installation package or merge module to be opened.  The <i>szDatabase</i> parameter cannot be <b>NULL</b>.

## -returns

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
The method succeeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>szDatabase</i> is invalid.

</td>
</tr>
</table>
 

This method can also return one or more of the errors returned by the <a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a> function. The error is converted to <b>HRESULTS</b> using the <b>HRESULT_FROM_WIN32</b> function.

## -remarks

The <b>OpenDatabase</b> method can also accept a handle to an opened database. The handle to the opened database can be provided in the form "#nnnn" where nnnn is the database handle in string form. For example, for an opened database handle 123, the method can accept #123 for the value of  <i>szDatabase</i>  instead of the path to the package.

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>