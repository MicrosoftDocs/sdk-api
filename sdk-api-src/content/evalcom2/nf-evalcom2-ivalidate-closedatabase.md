---
UID: NF:evalcom2.IValidate.CloseDatabase
title: IValidate::CloseDatabase
author: windows-sdk-content
description: The CloseDatabase method closes the currently open Windows Installer package or merge module. Windows Installer packages or merge modules can be opened by using the OpenDatabase method.
old-location: setup\ivalidate_closedatabase.htm
tech.root: msi
ms.assetid: 7124f467-4efd-4e8b-9ce2-8463779f6fb9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseDatabase, CloseDatabase method, CloseDatabase method,IValidate interface, IValidate interface,CloseDatabase method, IValidate.CloseDatabase, IValidate::CloseDatabase, evalcom2/IValidate::CloseDatabase, setup.ivalidate_closedatabase
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
 - IValidate.CloseDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IValidate::CloseDatabase


## -description


The <b>CloseDatabase</b> method closes the currently open Windows Installer package or merge module.  Windows Installer packages or merge modules can be opened by using the <a href="https://msdn.microsoft.com/3f295eea-5f6b-4afa-b0ac-55606086b2b2">OpenDatabase</a> method.


## -parameters






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
 

This method can also return one or more of the errors returned by the <a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a> function. The error is converted to <b>HRESULTS</b> using the <b>HRESULT_FROM_WIN32</b> function.




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

