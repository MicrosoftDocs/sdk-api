---
UID: NF:evalcom2.IValidate.SetDisplay
title: IValidate::SetDisplay
author: windows-sdk-content
description: The SetDisplay method enables an authoring tool to obtain ICE status messages through a callback function.
old-location: setup\ivalidate_setdisplay.htm
tech.root: MSI
ms.assetid: e376740e-82fc-44da-b200-c74d73978c6e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IValidate interface,SetDisplay method, IValidate.SetDisplay, IValidate::SetDisplay, SetDisplay, SetDisplay method, SetDisplay method,IValidate interface, evalcom2/IValidate::SetDisplay, setup.ivalidate_setdisplay
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IValidate.SetDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IValidate::SetDisplay


## -description


The <b>SetDisplay</b> method enables an authoring tool to obtain ICE status messages through a callback function.


## -parameters




### -param pDisplayFunction [in]

		Specifies a callback function that conforms to the <a href="https://msdn.microsoft.com/ff7b2789-a825-4fa4-b00c-a538f37d0eba">LPDISPLAYVAL</a> specification.


### -param pContext [in]

A pointer to an application context that is passed to the callback function. This parameter can be used for error checking.  The <i>pContext</i> parameter can be <b>NULL</b>.


## -returns



This method can return one of these values.

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
The <i>pDisplayFunction</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

