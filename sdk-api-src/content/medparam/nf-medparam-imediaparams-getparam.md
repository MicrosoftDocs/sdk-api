---
UID: NF:medparam.IMediaParams.GetParam
title: IMediaParams::GetParam
author: windows-sdk-content
description: The GetParam method retrieves the current value of the specified parameter. If the parameter is currently within an envelope segment, the returned value is the value on the most recently processed sample.
old-location: dshow\imediaparams_getparam.htm
tech.root: DirectShow
ms.assetid: 4fcae36a-c659-4565-9169-66d97beb26a4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetParam, GetParam method [DirectShow], GetParam method [DirectShow],IMediaParams interface, IMediaParams interface [DirectShow],GetParam method, IMediaParams.GetParam, IMediaParams::GetParam, IMediaParamsGetParam, dshow.imediaparams_getparam, medparam/IMediaParams::GetParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: medparam.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParams.GetParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaParams::GetParam


## -description



The <code>GetParam</code> method retrieves the current value of the specified parameter. If the parameter is currently within an envelope segment, the returned value is the value on the most recently processed sample.




## -parameters




### -param dwParamIndex [in]

Zero-based index of the parameter.


### -param pValue [out]

Pointer to a variable of type <b>MP_DATA</b> that receives the parameter value.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



To enumerate the parameters supported by this object, along with their index values, use the <a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/68ea8f6a-4b6d-4d79-a986-6032b767147b">IMediaParams Interface</a>
 

 

