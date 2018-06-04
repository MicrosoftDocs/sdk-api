---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPerPropertyBrowsing::GetPredefinedValue


## -description


Retrieves the value of the specified property that is associated with a predefined string name. This property is associated with a predefined string name as returned from <a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">IPerPropertyBrowsing::GetPredefinedStrings</a>. The predefined string is identified by a token returned from <b>GetPredefinedStrings</b>.



## -parameters




### -param dispID [in]

The dispatch identifier of the property for which a predefined value is requested.


### -param dwCookie [in]

A token identifying which value to return. The token was previously returned in the <i>pCaCookiesOut</i> array filled by <a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">GetPredefinedStrings</a>.


### -param pVarOut [out]

A pointer to the <b>VARIANT</b> value for the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The method completed succesfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This object does not support predefined strings or predefined values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pVarOut</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller is responsible for freeing any allocations contained in the <b>VARIANT</b>. Unless the <b>vt</b> member of <b>VARIANT</b> is VT_VARIANT, the caller can free memory using a single call to <b>VariantClear</b>. Otherwise, the caller must recursively free the contained <b>VARIANT</b> values before freeing the outer <b>VARIANT</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Support for predefined names and values is not required. If your object does not support these names, return E_NOTIMPL from this method. If this method is not implemented, <a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">IPerPropertyBrowsing::GetPredefinedStrings</a> must not be implemented either.

This method allocates any memory needed inside the <b>VARIANT</b>.




## -see-also




<a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a>
 

 

