---
UID: NF:oleacc.IAccPropServices.SetHwndPropServer
title: IAccPropServices::SetHwndPropServer (oleacc.h)
description: This method wraps SetPropServer, providing a convenient entry point for callers who are annotating HWND-based accessible elements.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetHwndPropServer method","IAccPropServices.SetHwndPropServer","IAccPropServices::SetHwndPropServer","SetHwndPropServer","SetHwndPropServer method [Windows Accessibility]","SetHwndPropServer method [Windows Accessibility]","IAccPropServices interface","_msaa_IAccPropServices_SetHwndPropServer","msaa.iaccpropservices_iaccpropservices__sethwndpropserver","oleacc/IAccPropServices::SetHwndPropServer","winauto.iaccpropservices_iaccpropservices__sethwndpropserver"]
old-location: winauto\iaccpropservices_iaccpropservices__sethwndpropserver.htm
tech.root: WinAuto
ms.assetid: 05dbdf97-9b1a-439f-b3a1-b517733ec0a8
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHwndPropServer method, IAccPropServices.SetHwndPropServer, IAccPropServices::SetHwndPropServer, SetHwndPropServer, SetHwndPropServer method [Windows Accessibility], SetHwndPropServer method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetHwndPropServer, msaa.iaccpropservices_iaccpropservices__sethwndpropserver, oleacc/IAccPropServices::SetHwndPropServer, winauto.iaccpropservices_iaccpropservices__sethwndpropserver
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
 - IAccPropServices::SetHwndPropServer
 - oleacc/IAccPropServices::SetHwndPropServer
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
 - IAccPropServices.SetHwndPropServer
---

# IAccPropServices::SetHwndPropServer


## -description

This method wraps <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>, providing a convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements.

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

Specifies an array of properties that is to be handled by the specified callback object.

### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.

### -param pServer [in]

Type: <b>IAccPropServer*</b>

Specifies the callback object, which will be invoked when a client requests one of the overridden properties.

### -param annoScope [in]

Type: <b>AnnoScope</b>

May be ANNO_THIS, indicating that the annotation affects the indicated accessible element only; or ANNO_CONTAINER, indicating that it applies to the element and its immediate element children.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported properties, if the identity string is not valid, or if <i>annoScope</i> is not one of ANNO_THIS or ANNO_CONTAINER.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhwndprops">ClearHwndProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">SetHwndProp</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">SetHwndPropStr</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>