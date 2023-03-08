---
UID: NF:evalcom2.IValidate.CloseDatabase
title: IValidate::CloseDatabase (evalcom2.h)
description: The CloseDatabase method closes the currently open Windows Installer package or merge module. Windows Installer packages or merge modules can be opened by using the OpenDatabase method.
helpviewer_keywords: ["CloseDatabase","CloseDatabase method","CloseDatabase method","IValidate interface","IValidate interface","CloseDatabase method","IValidate.CloseDatabase","IValidate::CloseDatabase","evalcom2/IValidate::CloseDatabase","setup.ivalidate_closedatabase"]
old-location: setup\ivalidate_closedatabase.htm
tech.root: setup
ms.assetid: 7124f467-4efd-4e8b-9ce2-8463779f6fb9
ms.date: 12/05/2018
ms.keywords: CloseDatabase, CloseDatabase method, CloseDatabase method,IValidate interface, IValidate interface,CloseDatabase method, IValidate.CloseDatabase, IValidate::CloseDatabase, evalcom2/IValidate::CloseDatabase, setup.ivalidate_closedatabase
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
 - IValidate::CloseDatabase
 - evalcom2/IValidate::CloseDatabase
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
 - IValidate.CloseDatabase
---

# IValidate::CloseDatabase


## -description

The <b>CloseDatabase</b> method closes the currently open Windows Installer package or merge module.  Windows Installer packages or merge modules can be opened by using the <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase">OpenDatabase</a> method.



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
</table>
 

This method can also return one or more of the errors returned by the <a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function. The error is converted to <b>HRESULTS</b> using the <b>HRESULT_FROM_WIN32</b> function.

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>
