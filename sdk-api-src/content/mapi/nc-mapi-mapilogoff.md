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

# MAPILOGOFF callback function


## -description


<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPILogoff</b> function ends a session with the messaging system.


## -parameters




### -param lhSession [in]

Handle for the Simple MAPI session to be terminated. Session handles are returned by the <a href="https://msdn.microsoft.com/5a61f0f2-347e-40fb-b7f9-6b42690cbcd8">MAPILogon</a> function and invalidated by <b>MAPILogoff</b>. The value of the <i>lhSession</i> parameter must represent a valid session; it cannot be zero.


### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.


### -param flFlags

Reserved; must be zero.


### -param ulReserved

Reserved; must be zero.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
The <i>flFlags</i> parameter is invalid or one or more unspecified errors occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. The session was not terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was used for the <i>lhSession</i> parameter. The session was not terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the session was terminated.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5a61f0f2-347e-40fb-b7f9-6b42690cbcd8">MAPILogon</a>



<a href="https://msdn.microsoft.com/a8330f38-3ef0-4b36-a5e7-89837088cbef">Simple MAPI</a>
 

 

