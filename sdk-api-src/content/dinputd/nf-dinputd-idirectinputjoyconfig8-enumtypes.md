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

# IDirectInputJoyConfig8::EnumTypes


## -description


The <b>IDirectInputJoyConfig8::EnumTypes </b>method enumerates the joystick types currently supported by DirectInput. A joystick type describes how DirectInput should communicate with a joystick device. It includes information such as the presence and location of each of the axes and the number of buttons supported by the device. 


## -parameters




### -param






#### - lpCallback

Points to an application-defined callback function that receives the DirectInput joystick types. See the Remarks section for the function prototype. 


#### - pvRef

Specifies a 32-bit application-defined value to be passed to the callback function. This value can be any 32-bit value; it is prototyped as an LPVOID for convenience. 


## -returns



Returns DI_OK if successful; otherwise, returns one of the following COM error values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
</table>
 




## -remarks



This callback receives DirectInput joystick types as a result of a call to the IDirectInputJoyConfig8::EnumTypes method.

<pre class="syntax" xml:space="preserve"><code>

/*
Parameters
pwszTypeName 
Points to the name of the joystick type. A buffer of MAX_JOYSTRING characters is sufficient to hold the type name. The type name should never be shown to the end user; instead, the "display name" should be shown. Use IDirectInputJoyConfig8::GetTypeInfo to obtain the display name of a joystick type. Type names that begin with a pound sign ("#") represent predefined types that cannot be modified or deleted. 

pvRef 
Points to the application-defined value given in the IDirectInputJoyConfig8::EnumTypes method.

Return value
Returns a BOOL value, DIENUM_CONTINUE, to continue the enumeration, or DIENUM_STOP to stop the enumeration. 

*/


BOOL DIEnumJoyTypeProc(
   LPCWSTR pwszTypeName,
   LPVOID  pvRef
);
 


</code></pre>


