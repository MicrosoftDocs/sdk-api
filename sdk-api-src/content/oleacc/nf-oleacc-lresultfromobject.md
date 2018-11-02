---
UID: NF:oleacc.LresultFromObject
title: LresultFromObject function
author: windows-sdk-content
description: Returns a reference, similar to a handle, to the specified object. Servers return this reference when handling WM_GETOBJECT.
old-location: winauto\lresultfromobject.htm
tech.root: WinAuto
ms.assetid: c219a4cd-7a8f-4942-8975-b3d823b6497f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: LresultFromObject, LresultFromObject function [Windows Accessibility], _msaa_LresultFromObject, msaa.lresultfromobject, oleacc/LresultFromObject, winauto.lresultfromobject
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
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - LresultFromObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# LresultFromObject function


## -description


Returns a reference, similar to a handle, to the specified object. Servers return this reference when handling <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a>.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the interface provided to the client. This parameter is IID_IAccessible.


### -param wParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

Value sent by the associated <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message in its <i>wParam</i> parameter.


### -param punk [in]

Type: <b>LPUNKNOWN</b>

Address of the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface to the object that corresponds to the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LRESULT</a></b>

If successful, returns a positive value that is a reference to the object.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

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



Servers call this function only when handling the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message. For an overview of how <b>LresultFromObject</b> is related to <b>WM_GETOBJECT</b>, see <a href="https://msdn.microsoft.com/53f7b3db-97e4-4ff2-9f7a-4555ec7956ea">How WM_GETOBJECT Works</a>.

<b>LresultFromObject</b> increments the object's reference count. If you are not storing the interface pointer passed to the function (that is, you create a new interface pointer for the object each time <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> is received), call the object's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to decrement the reference count back to one. Then the client calls <b>Release</b> and the object is destroyed. For more information, see <a href="https://msdn.microsoft.com/455398b7-f748-4ab0-8953-3f74439e44f1">How to Handle WM_GETOBJECT</a>.

Each time a server processes <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> for a specific object, it calls <b>LresultFromObject</b> to obtain a new reference to the object. Servers do not save the reference returned from <b>LresultFromObject</b> from one instance of processing <b>WM_GETOBJECT</b> to use as the message's return value when processing subsequent <b>WM_GETOBJECT</b> messages for the same object. This causes the client to receive an error.




## -see-also




<a href="https://msdn.microsoft.com/d140206a-9918-438b-96bd-df141da2f04b">Creating Proxy Objects</a>



<a href="https://msdn.microsoft.com/53f7b3db-97e4-4ff2-9f7a-4555ec7956ea">How WM_GETOBJECT Works</a>



<a href="https://msdn.microsoft.com/455398b7-f748-4ab0-8953-3f74439e44f1">How to Handle WM_GETOBJECT</a>



<a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a>
 

 

