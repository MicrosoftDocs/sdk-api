---
UID: NF:oleacc.IAccPropServices.SetPropValue
title: IAccPropServices::SetPropValue (oleacc.h)
description: Use SetPropValue to identify the accessible element to be annotated, specify the property to be annotated, and provide a new value for that property.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetPropValue method","IAccPropServices.SetPropValue","IAccPropServices::SetPropValue","SetPropValue","SetPropValue method [Windows Accessibility]","SetPropValue method [Windows Accessibility]","IAccPropServices interface","_msaa_IAccPropServices_SetPropValue","msaa.iaccpropservices_iaccpropservices__setpropvalue","oleacc/IAccPropServices::SetPropValue","winauto.iaccpropservices_iaccpropservices__setpropvalue"]
old-location: winauto\iaccpropservices_iaccpropservices__setpropvalue.htm
tech.root: WinAuto
ms.assetid: c86acb70-fa77-4f95-8a99-e60872cdaa7e
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetPropValue method, IAccPropServices.SetPropValue, IAccPropServices::SetPropValue, SetPropValue, SetPropValue method [Windows Accessibility], SetPropValue method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetPropValue, msaa.iaccpropservices_iaccpropservices__setpropvalue, oleacc/IAccPropServices::SetPropValue, winauto.iaccpropservices_iaccpropservices__setpropvalue
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
req.lib: 
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccPropServices::SetPropValue
 - oleacc/IAccPropServices::SetPropValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.SetPropValue
---

# IAccPropServices::SetPropValue


## -description

Use <b>SetPropValue</b> to identify the accessible element to be annotated, specify the property to be annotated, and provide a new value for that property.

If server developers know the <b>HWND</b> of the accessible element they want to annotate, they can use one of the following methods:
<ul>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">IAccPropServices::SetHwndPropStr</a>,</li>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">IAccPropServices::SetHwndProp</a>, or</li>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">IAccPropServices::SetHwndPropServer</a>
</li>
</ul>

## -parameters

### -param pIDString [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

Identifies the accessible element that is to be annotated.

### -param dwIDStringLen [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the length of the string identified by the <i>pIDString</i> parameter.

### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies the property of the accessible element to be annotated.

### -param var [in]

Type: <b>VARIANT</b>

Specifies a new value for the property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>idProp</i> is not a supported property, if <i>var</i> is not a supported type for that property, or if the identity string is not valid.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

See the support section for a list of supported properties and their expected types. Note that currently some properties are supported only when a callback is used and cannot be specified directly using this method.