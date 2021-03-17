---
UID: NF:oleacc.IAccPropServices.SetHwndPropStr
title: IAccPropServices::SetHwndPropStr (oleacc.h)
description: This method wraps SetPropValue, providing a more convenient entry point for callers who are annotating HWND-based accessible elements.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetHwndPropStr method","IAccPropServices.SetHwndPropStr","IAccPropServices::SetHwndPropStr","SetHwndPropStr","SetHwndPropStr method [Windows Accessibility]","SetHwndPropStr method [Windows Accessibility]","IAccPropServices interface","_msaa_IAccPropServices_SetHwndPropStr","msaa.iaccpropservices_iaccpropservices__sethwndpropstr","oleacc/IAccPropServices::SetHwndPropStr","winauto.iaccpropservices_iaccpropservices__sethwndpropstr"]
old-location: winauto\iaccpropservices_iaccpropservices__sethwndpropstr.htm
tech.root: WinAuto
ms.assetid: 68f09a23-56b2-4fae-98a2-616b17fb4e1f
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHwndPropStr method, IAccPropServices.SetHwndPropStr, IAccPropServices::SetHwndPropStr, SetHwndPropStr, SetHwndPropStr method [Windows Accessibility], SetHwndPropStr method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetHwndPropStr, msaa.iaccpropservices_iaccpropservices__sethwndpropstr, oleacc/IAccPropServices::SetHwndPropStr, winauto.iaccpropservices_iaccpropservices__sethwndpropstr
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
 - IAccPropServices::SetHwndPropStr
 - oleacc/IAccPropServices::SetHwndPropStr
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
 - IAccPropServices.SetHwndPropStr
---

# IAccPropServices::SetHwndPropStr


## -description

This method wraps <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>, providing a more convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements.

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

### -param str [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Specifies a new value for that property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhwndprops">ClearHwndProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">SetHwndProp</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">SetHwndPropServer</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>