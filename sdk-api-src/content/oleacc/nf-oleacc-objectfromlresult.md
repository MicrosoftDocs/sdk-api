---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ObjectFromLresult function


## -description


Retrieves a requested interface pointer for an accessible object based on a previously generated object reference.

This function is designed for internal use by Microsoft Active Accessibility and is documented for informational purposes only. Neither clients nor servers should call this function.


## -parameters




### -param lResult [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LRESULT</a></b>

A 32-bit value returned by a previous successful call to the <a href="https://msdn.microsoft.com/c219a4cd-7a8f-4942-8975-b3d823b6497f">LresultFromObject</a> function.


### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the interface to be retrieved. This is IID_IAccessible.


### -param wParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

Value sent by the associated <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message in its <i>wParam</i> parameter. 
			 


### -param ppvObject [out]

Type: <b>void**</b>

Receives the address of the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface on the object that corresponds to the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error codes</a>.

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
One or more arguments are not valid. This occurs when the <i>lResult</i> parameter specified is not a value obtained by a call to <a href="https://msdn.microsoft.com/c219a4cd-7a8f-4942-8975-b3d823b6497f">LresultFromObject</a>, or when <i>lResult</i> is a value used on a previous call to <a href="https://msdn.microsoft.com/97e766fd-e142-40d1-aba7-408b45d33426">ObjectFromLresult</a>.

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




<a href="https://msdn.microsoft.com/56ab7e6b-a469-49f9-ab56-82e11e374b25">WM_GETOBJECT Window Message</a>
 

 

