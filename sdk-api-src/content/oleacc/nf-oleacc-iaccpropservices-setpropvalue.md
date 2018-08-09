---
UID: NF:oleacc.IAccPropServices.SetPropValue
title: IAccPropServices::SetPropValue
author: windows-sdk-content
description: Use SetPropValue to identify the accessible element to be annotated, specify the property to be annotated, and provide a new value for that property.
old-location: winauto\iaccpropservices_iaccpropservices__setpropvalue.htm
old-project: WinAuto
ms.assetid: c86acb70-fa77-4f95-8a99-e60872cdaa7e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetPropValue method, IAccPropServices.SetPropValue, IAccPropServices::SetPropValue, SetPropValue, SetPropValue method [Windows Accessibility], SetPropValue method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetPropValue, msaa.iaccpropservices_iaccpropservices__setpropvalue, oleacc/IAccPropServices::SetPropValue, winauto.iaccpropservices_iaccpropservices__setpropvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.SetPropValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
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



