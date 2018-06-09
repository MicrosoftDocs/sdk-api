---
UID: NF:dmoreg.DMOGetTypes
title: DMOGetTypes function
author: windows-sdk-content
description: The DMOGetTypes function retrieves the name of a DMO from the registry.
old-location: dshow\dmogettypes.htm
old-project: DirectShow
ms.assetid: d50e067e-6bf2-4d19-86ef-38a414099666
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DMOGetTypes, DMOGetTypes function [DirectShow], dmoreg/DMOGetTypes, dshow.dmogettypes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - DMOGetTypes
product: Windows
targetos: Windows
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
---

# DMOGetTypes function


## -description


The <b>DMOGetTypes</b> function retrieves the name of a DMO from the registry.


## -parameters




### -param clsidDMO

Class identifier (CLSID) of the DMO.


### -param ulInputTypesRequested

Size of the array passed in the <i>pInputTypes</i> parameter.


### -param pulInputTypesSupplied

Pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/53bf4c34-d180-4edd-b59a-55d7d90708b5">DMO_PARTIAL_MEDIATYPE</a> structures in <i>pInputTypes</i> that the function fills in.


### -param pInputTypes

Pointer to a caller-allocated array of DMO_PARTIAL_MEDIATYPE structures. The size of the array is given in the ulInputTypesRequested parameter. The function fills the array with the input types registered for the DMO.


### -param ulOutputTypesRequested

Size of the array passed in the <i>pOutputTypes</i> parameter.


### -param pulOutputTypesSupplied

Pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/53bf4c34-d180-4edd-b59a-55d7d90708b5">DMO_PARTIAL_MEDIATYPE</a> structures in <i>pOutputTypes</i> that the function fills in.


### -param pOutputTypes

Pointer to a caller-allocated array of <a href="https://msdn.microsoft.com/53bf4c34-d180-4edd-b59a-55d7d90708b5">DMO_PARTIAL_MEDIATYPE</a> structures. The size of the array is given in the <i>ulOutputTypesRequested</i> parameter. The function fills the array with the DMO output types registered for the DMO.


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
Array too small.

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



If one of the arrays is too small to hold all of the registered types, the function fills the array but returns S_FALSE.

If the DMO did not register any media types, the function returns S_OK and sets <i>*pulInputTypesSupplied</i> and <i>*pulOutputTypesSupplied</i> to zero.




## -see-also




<a href="https://msdn.microsoft.com/0a380dc0-23f0-4ef0-898a-3b5afddf5eaa">DMO Functions</a>
 

 

