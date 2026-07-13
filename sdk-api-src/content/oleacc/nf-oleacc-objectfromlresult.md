---
UID: NF:oleacc.ObjectFromLresult
title: ObjectFromLresult function (oleacc.h)
description: Retrieves a requested interface pointer for an accessible object based on a previously generated object reference.
helpviewer_keywords: ["ObjectFromLresult","ObjectFromLresult function [Windows Accessibility]","_msaa_ObjectFromLresult","msaa.objectfromlresult","oleacc/ObjectFromLresult","winauto.objectfromlresult"]
old-location: winauto\objectfromlresult.htm
tech.root: WinAuto
ms.assetid: 97e766fd-e142-40d1-aba7-408b45d33426
ms.date: 12/05/2018
ms.keywords: ObjectFromLresult, ObjectFromLresult function [Windows Accessibility], _msaa_ObjectFromLresult, msaa.objectfromlresult, oleacc/ObjectFromLresult, winauto.objectfromlresult
req.header: oleacc.h
req.include-header: 
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - ObjectFromLresult
 - oleacc/ObjectFromLresult
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
 - ObjectFromLresult
---

# ObjectFromLresult function


## -description

Retrieves a requested interface pointer for an accessible object based on a previously generated object reference.

This function is designed for internal use by Microsoft Active Accessibility and is documented for informational purposes only. Neither clients nor servers should call this function.

## -parameters

### -param lResult [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LRESULT</a></b>

A 32-bit value returned by a previous successful call to the <a href="/windows/desktop/api/oleacc/nf-oleacc-lresultfromobject">LresultFromObject</a> function.

### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the interface to be retrieved. This is IID_IAccessible.

### -param wParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

Value sent by the associated [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message in its <i>wParam</i> parameter.

### -param ppvObject [out]

Type: <b>void**</b>

Receives the address of the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface on the object that corresponds to the [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following standard <a href="/windows/desktop/WinAuto/return-values">COM error codes</a>.

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
One or more arguments are not valid. This occurs when the <i>lResult</i> parameter specified is not a value obtained by a call to <a href="/windows/desktop/api/oleacc/nf-oleacc-lresultfromobject">LresultFromObject</a>, or when <i>lResult</i> is a value used on a previous call to <a href="/windows/desktop/api/oleacc/nf-oleacc-objectfromlresult">ObjectFromLresult</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object specified in the <i>ppvObject</i> parameter does not support the interface specified by the <i>riid</i> parameter.

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

## -see-also

[WM_GETOBJECT](/windows/win32/winauto/wm-getobject)