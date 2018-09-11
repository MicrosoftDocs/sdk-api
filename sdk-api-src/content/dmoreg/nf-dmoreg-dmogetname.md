---
UID: NF:dmoreg.DMOGetName
title: DMOGetName function
author: windows-sdk-content
description: The DMOGetName function retrieves the name of a DMO from the registry.
old-location: dshow\dmogetname.htm
tech.root: DirectShow
ms.assetid: 7cb803c2-4fe1-46e3-868d-1b7c28b07a5b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DMOGetName, DMOGetName function [DirectShow], dmoreg/DMOGetName, dshow.dmogetname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dmoreg.h
req.include-header: Dmo.h
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - DMOGetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DMOGetName function


## -description


The <b>DMOGetName</b> function retrieves the name of a DMO from the registry.


## -parameters




### -param clsidDMO

Class identifier (CLSID) of the DMO.


### -param szName

Array of 80 Unicode characters that receives the name of the DMO. The caller must allocate the array. The name is a NULL-terminated string.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No name was registered for this DMO, or the name has zero length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



If the method returns S_FALSE, <i>szName</i> is set to '\0'.




## -see-also




<a href="https://msdn.microsoft.com/0a380dc0-23f0-4ef0-898a-3b5afddf5eaa">DMO Functions</a>
 

 

