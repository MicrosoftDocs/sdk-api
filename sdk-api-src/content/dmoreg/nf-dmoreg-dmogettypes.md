---
UID: NF:dmoreg.DMOGetTypes
title: DMOGetTypes function (dmoreg.h)
description: The DMOGetTypes function retrieves the name of a DMO from the registry.
helpviewer_keywords: ["DMOGetTypes","DMOGetTypes function [DirectShow]","dmoreg/DMOGetTypes","dshow.dmogettypes"]
old-location: dshow\dmogettypes.htm
tech.root: dshow
ms.assetid: d50e067e-6bf2-4d19-86ef-38a414099666
ms.date: 12/05/2018
ms.keywords: DMOGetTypes, DMOGetTypes function [DirectShow], dmoreg/DMOGetTypes, dshow.dmogettypes
f1_keywords:
- dmoreg/DMOGetTypes
dev_langs:
- c++
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
- DMOGetTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Pointer to a variable that receives the number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dmoreg/ns-dmoreg-dmo_partial_mediatype">DMO_PARTIAL_MEDIATYPE</a> structures in <i>pInputTypes</i> that the function fills in.


### -param pInputTypes

Pointer to a caller-allocated array of DMO_PARTIAL_MEDIATYPE structures. The size of the array is given in the ulInputTypesRequested parameter. The function fills the array with the input types registered for the DMO.


### -param ulOutputTypesRequested

Size of the array passed in the <i>pOutputTypes</i> parameter.


### -param pulOutputTypesSupplied

Pointer to a variable that receives the number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dmoreg/ns-dmoreg-dmo_partial_mediatype">DMO_PARTIAL_MEDIATYPE</a> structures in <i>pOutputTypes</i> that the function fills in.


### -param pOutputTypes

Pointer to a caller-allocated array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dmoreg/ns-dmoreg-dmo_partial_mediatype">DMO_PARTIAL_MEDIATYPE</a> structures. The size of the array is given in the <i>ulOutputTypesRequested</i> parameter. The function fills the array with the DMO output types registered for the DMO.


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dmo-functions">DMO Functions</a>
 

 

