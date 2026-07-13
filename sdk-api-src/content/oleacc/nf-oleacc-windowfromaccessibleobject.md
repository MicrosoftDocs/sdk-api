---
UID: NF:oleacc.WindowFromAccessibleObject
title: WindowFromAccessibleObject function (oleacc.h)
description: Retrieves the window handle that corresponds to a particular instance of an IAccessible interface.
helpviewer_keywords: ["WindowFromAccessibleObject","WindowFromAccessibleObject function [Windows Accessibility]","_msaa_WindowFromAccessibleObject","msaa.windowfromaccessibleobject","oleacc/WindowFromAccessibleObject","winauto.windowfromaccessibleobject"]
old-location: winauto\windowfromaccessibleobject.htm
tech.root: WinAuto
ms.assetid: b3a3d3dd-ef84-4323-ab6d-6331d8389f11
ms.date: 12/05/2018
ms.keywords: WindowFromAccessibleObject, WindowFromAccessibleObject function [Windows Accessibility], _msaa_WindowFromAccessibleObject, msaa.windowfromaccessibleobject, oleacc/WindowFromAccessibleObject, winauto.windowfromaccessibleobject
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
 - WindowFromAccessibleObject
 - oleacc/WindowFromAccessibleObject
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
api_name:
 - WindowFromAccessibleObject
---

# WindowFromAccessibleObject function


## -description

Retrieves the window handle that corresponds to a particular instance of an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface.

## -parameters

### -param unnamedParam1 [in]

Type: <b>IAccessible*</b>

Pointer to the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface whose corresponding window handle will be retrieved. This parameter must not be <b>NULL</b>.

### -param phwnd [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a>*</b>

Address of a variable that receives a handle to the window containing the object specified in <i>pacc</i>. If this value is <b>NULL</b> after the call, the object is not contained within a window; for example, the mouse pointer is not contained within a window.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns the following or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

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
An argument is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfromwindow">AccessibleObjectFromWindow</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>