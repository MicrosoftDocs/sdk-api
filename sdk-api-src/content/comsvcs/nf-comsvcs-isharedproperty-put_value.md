---
UID: NF:comsvcs.ISharedProperty.put_Value
title: ISharedProperty::put_Value (comsvcs.h)
author: windows-sdk-content
description: Sets the value of a shared property.
old-location: cos\isharedproperty_put_value.htm
tech.root: cossdk
ms.assetid: d193990c-a804-41aa-81d7-75aced274f73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISharedProperty interface [COM+],put_Value method, ISharedProperty.put_Value, ISharedProperty::put_Value, _cos_ISharedProperty_put_Value, comsvcs/ISharedProperty::put_Value, cos.isharedproperty_put_value, put_Value, put_Value method [COM+], put_Value method [COM+],ISharedProperty interface
ms.topic: method
f1_keywords: 
 - "comsvcs/ISharedProperty.put_Value"
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedProperty.put_Value
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharedProperty::put_Value


## -description


Sets the value of a shared property.


## -parameters




### -param val [in]

The new value that is to be set for this shared property. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in the parameter contains an array that is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in the parameter is not a valid Variant type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isharedproperty">ISharedProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/sharedproperty">SharedProperty</a>
 

 

