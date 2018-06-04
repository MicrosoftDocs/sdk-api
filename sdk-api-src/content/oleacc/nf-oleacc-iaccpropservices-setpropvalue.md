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

# IAccPropServices::SetPropValue


## -description


Use <b>SetPropValue</b> to identify the accessible element to be annotated, specify the property to be annotated, and provide a new value for that property.

If server developers know the <b>HWND</b> of the accessible element they want to annotate, they can use one of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">IAccPropServices::SetHwndPropStr</a>,</li>
<li>
<a href="https://msdn.microsoft.com/00387897-5385-467d-9da4-4d71fce742b6">IAccPropServices::SetHwndProp</a>, or</li>
<li>
<a href="https://msdn.microsoft.com/05dbdf97-9b1a-439f-b3a1-b517733ec0a8">IAccPropServices::SetHwndPropServer</a>
</li>
</ul>

## -parameters




### -param pIDString [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Identifies the accessible element that is to be annotated.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of the string identified by the <i>pIDString</i> parameter.


### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies the property of the accessible element to be annotated.


### -param var [in]

Type: <b>VARIANT</b>

Specifies a new value for the property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>idProp</i> is not a supported property, if <i>var</i> is not a supported type for that property, or if the identity string is not valid.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



See the support section for a list of supported properties and their expected types. Note that currently some properties are supported only when a callback is used and cannot be specified directly using this method.



