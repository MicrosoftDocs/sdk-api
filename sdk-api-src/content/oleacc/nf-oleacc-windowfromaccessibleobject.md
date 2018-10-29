---
UID: NF:oleacc.WindowFromAccessibleObject
title: WindowFromAccessibleObject function
author: windows-sdk-content
description: Retrieves the window handle that corresponds to a particular instance of an IAccessible interface.
old-location: winauto\windowfromaccessibleobject.htm
tech.root: WinAuto
ms.assetid: b3a3d3dd-ef84-4323-ab6d-6331d8389f11
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WindowFromAccessibleObject, WindowFromAccessibleObject function [Windows Accessibility], _msaa_WindowFromAccessibleObject, msaa.windowfromaccessibleobject, oleacc/WindowFromAccessibleObject, winauto.windowfromaccessibleobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - WindowFromAccessibleObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# WindowFromAccessibleObject function


## -description


Retrieves the window handle that corresponds to a particular instance of an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface.


## -parameters




### -param arg1 [in]

Type: <b>IAccessible*</b>

Pointer to the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface whose corresponding window handle will be retrieved. This parameter must not be <b>NULL</b>.


### -param phwnd [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>*</b>

Address of a variable that receives a handle to the window containing the object specified in <i>pacc</i>. If this value is <b>NULL</b> after the call, the object is not contained within a window; for example, the mouse pointer is not contained within a window.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns the following or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

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




<a href="https://msdn.microsoft.com/297ac50f-2a58-477b-ba57-5d1416c191b3">AccessibleObjectFromWindow</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>
 

 

