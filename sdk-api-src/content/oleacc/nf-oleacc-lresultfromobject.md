---
UID: NF:oleacc.LresultFromObject
title: LresultFromObject function (oleacc.h)
description: Returns a reference, similar to a handle, to the specified object. Servers return this reference when handling WM_GETOBJECT.
helpviewer_keywords: ["LresultFromObject","LresultFromObject function [Windows Accessibility]","_msaa_LresultFromObject","msaa.lresultfromobject","oleacc/LresultFromObject","winauto.lresultfromobject"]
old-location: winauto\lresultfromobject.htm
tech.root: WinAuto
ms.assetid: c219a4cd-7a8f-4942-8975-b3d823b6497f
ms.date: 12/05/2018
ms.keywords: LresultFromObject, LresultFromObject function [Windows Accessibility], _msaa_LresultFromObject, msaa.lresultfromobject, oleacc/LresultFromObject, winauto.lresultfromobject
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - LresultFromObject
 - oleacc/LresultFromObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-oleacc-l1-1-2.dll
 - Oleacc.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - LresultFromObject
---

# LresultFromObject function


## -description

Returns a reference, similar to a handle, to the specified object. Servers return this reference when handling <a href="/windows/desktop/WinAuto/wm-getobject">WM_GETOBJECT</a>.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the interface provided to the client. This parameter is IID_IAccessible.

### -param wParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

Value sent by the associated [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message in its <i>wParam</i> parameter.

### -param punk [in]

Type: <b>LPUNKNOWN</b>

Address of the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface to the object that corresponds to the [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LRESULT</a></b>

If successful, returns a positive value that is a reference to the object.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

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
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object specified in the <i>pAcc</i> parameter does not support the interface specified in the <i>riid</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to store the object reference.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>

## -remarks

Servers call this function only when handling the [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message. For an overview of how <b>LresultFromObject</b> is related to <b>WM_GETOBJECT</b>, see <a href="/windows/desktop/WinAuto/how-wm-getobject-works">How WM_GETOBJECT Works</a>.

<b>LresultFromObject</b> increments the object's reference count. If you are not storing the interface pointer passed to the function (that is, you create a new interface pointer for the object each time [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) is received), call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to decrement the reference count back to one. Then the client calls <b>Release</b> and the object is destroyed. For more information, see <a href="/windows/desktop/WinAuto/how-to-handle-wm-getobject">How to Handle WM_GETOBJECT</a>.

Each time a server processes [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) for a specific object, it calls <b>LresultFromObject</b> to obtain a new reference to the object. Servers do not save the reference returned from <b>LresultFromObject</b> from one instance of processing <b>WM_GETOBJECT</b> to use as the message's return value when processing subsequent <b>WM_GETOBJECT</b> messages for the same object. This causes the client to receive an error.

## -see-also

<a href="/windows/desktop/WinAuto/creating-proxy-objects">Creating Proxy Objects</a>

<a href="/windows/desktop/WinAuto/how-wm-getobject-works">How WM_GETOBJECT Works</a>

<a href="/windows/desktop/WinAuto/how-to-handle-wm-getobject">How to Handle WM_GETOBJECT</a>

[WM_GETOBJECT](/windows/win32/winauto/wm-getobject)