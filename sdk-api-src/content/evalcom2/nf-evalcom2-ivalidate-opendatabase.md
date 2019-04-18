---
UID: NF:evalcom2.IValidate.OpenDatabase
title: IValidate::OpenDatabase (evalcom2.h)
author: windows-sdk-content
description: The OpenDatabase method opens a Windows Installer installation package or merge module for validation.
old-location: setup\ivalidate_opendatabase.htm
tech.root: Msi
ms.assetid: 3f295eea-5f6b-4afa-b0ac-55606086b2b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IValidate interface,OpenDatabase method, IValidate.OpenDatabase, IValidate::OpenDatabase, OpenDatabase, OpenDatabase method, OpenDatabase method,IValidate interface, evalcom2/IValidate::OpenDatabase, setup.ivalidate_opendatabase
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Evalcom2.dll
api_name:
 - IValidate.OpenDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

This method can also return one or more of the errors returned by the <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> function. The error is converted to <b>HRESULTS</b> using the <b>HRESULT_FROM_WIN32</b> function.




## -remarks



The <b>OpenDatabase</b> method can also accept a handle to an opened database. The handle to the opened database can be provided in the form "#nnnn" where nnnn is the database handle in string form. For example, for an opened database handle 123, the method can accept #123 for the value of  <i>szDatabase</i>  instead of the path to the package. 




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

