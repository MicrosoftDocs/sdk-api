---
UID: NF:oleacc.IAccPropServices.ClearHwndProps
title: IAccPropServices::ClearHwndProps (oleacc.h)
description: This method wraps SetPropValue, SetPropServer, and ClearProps, and provides a convenient entry point for callers who are annotating HWND-based accessible elements.
helpviewer_keywords: ["ClearHwndProps","ClearHwndProps method [Windows Accessibility]","ClearHwndProps method [Windows Accessibility]","IAccPropServices interface","IAccPropServices interface [Windows Accessibility]","ClearHwndProps method","IAccPropServices.ClearHwndProps","IAccPropServices::ClearHwndProps","_msaa_IAccPropServices_ClearHwndProps","msaa.iaccpropservices_iaccpropservices__clearhwndprops","oleacc/IAccPropServices::ClearHwndProps","winauto.iaccpropservices_iaccpropservices__clearhwndprops"]
old-location: winauto\iaccpropservices_iaccpropservices__clearhwndprops.htm
tech.root: WinAuto
ms.assetid: 7fd3f595-4897-481f-972e-04cf1a4c6046
ms.date: 12/05/2018
ms.keywords: ClearHwndProps, ClearHwndProps method [Windows Accessibility], ClearHwndProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearHwndProps method, IAccPropServices.ClearHwndProps, IAccPropServices::ClearHwndProps, _msaa_IAccPropServices_ClearHwndProps, msaa.iaccpropservices_iaccpropservices__clearhwndprops, oleacc/IAccPropServices::ClearHwndProps, winauto.iaccpropservices_iaccpropservices__clearhwndprops
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
 - IAccPropServices::ClearHwndProps
 - oleacc/IAccPropServices::ClearHwndProps
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
 - IAccPropServices.ClearHwndProps
---

# IAccPropServices::ClearHwndProps


## -description

This method wraps <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>, and <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a>, and provides a convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements.

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

### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specifies an array of properties that is to be reset. These properties will revert to the default behavior that they displayed before they were annotated.

### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already-cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.

For descriptions of return values, see the corresponding <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>, or <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a> method.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

Additionally, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">SetHwndPropStr</a> takes a regular Unicode string as a parameter; the caller does not need to specially allocate a <b>BSTR</b>.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">SetHwndProp</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">SetHwndPropServer</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">SetHwndPropStr</a>