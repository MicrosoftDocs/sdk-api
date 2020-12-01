---
UID: NF:oleacc.IAccPropServices.SetHwndProp
title: IAccPropServices::SetHwndProp (oleacc.h)
description: This method wraps SetPropValue, providing a convenient entry point for callers who are annotating HWND-based accessible elements. If the new value is a string, you can use IAccPropServices::SetHwndPropStr instead.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetHwndProp method","IAccPropServices.SetHwndProp","IAccPropServices::SetHwndProp","SetHwndProp","SetHwndProp method [Windows Accessibility]","SetHwndProp method [Windows Accessibility]","IAccPropServices interface","_msaa_IAccPropServices_SetHwndProp","msaa.iaccpropservices_iaccpropservices__sethwndprop","oleacc/IAccPropServices::SetHwndProp","winauto.iaccpropservices_iaccpropservices__sethwndprop"]
old-location: winauto\iaccpropservices_iaccpropservices__sethwndprop.htm
tech.root: WinAuto
ms.assetid: 00387897-5385-467d-9da4-4d71fce742b6
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHwndProp method, IAccPropServices.SetHwndProp, IAccPropServices::SetHwndProp, SetHwndProp, SetHwndProp method [Windows Accessibility], SetHwndProp method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetHwndProp, msaa.iaccpropservices_iaccpropservices__sethwndprop, oleacc/IAccPropServices::SetHwndProp, winauto.iaccpropservices_iaccpropservices__sethwndprop
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
 - IAccPropServices::SetHwndProp
 - oleacc/IAccPropServices::SetHwndProp
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
 - IAccPropServices.SetHwndProp
---

# IAccPropServices::SetHwndProp


## -description

This method wraps <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>, providing a convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements. If the new value is a string, you can use <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">IAccPropServices::SetHwndPropStr</a> instead.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.

### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies which property of that element is to be annotated.

### -param var [in]

Type: <b>VARIANT</b>

Specifies a new value for that property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if the <i>idProp</i> property is not supported.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhwndprops">ClearHwndProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">SetHwndPropServer</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">SetHwndPropStr</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>