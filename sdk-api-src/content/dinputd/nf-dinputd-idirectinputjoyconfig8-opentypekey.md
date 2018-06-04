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

# IDirectInputJoyConfig8::OpenTypeKey


## -description


The <b>IDirectInputJoyConfig8::OpenTypeKey </b>method opens the registry key associated with a joystick type. 


## -parameters




### -param






#### - phk

Points to the opened registry key, on success. 


#### - pwszType

Points to the name of the type. The name of the type cannot exceed MAX_PATH characters, including the terminating null character. The name cannot begin with a "#" character. Types beginning with "#" are reserved by DirectInput. 


#### - regsam

Specifies a registry security access mask. This can be any of the values permitted by the <b>RegOpenKeyEx</b> function. If write access is requested, then joystick configuration must first have been acquired. If only read access is requested, then acquisition is not required. 


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
<dt><b>DIERR_NOTACQUIRED </b></dt>
</dl>
</td>
<td width="60%">
Joystick configuration has not been acquired. You must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540978">IDirectInputJoyConfig8::Acquire</a> before you can open a joystick type configuration key for writing. 

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>MAKE_HRESULT(SEVERITY_ERROR, FACILITY_WIN32, ErrorCode) </b></dt>
</dl>
</td>
<td width="60%">
A Win32 error code if access to the key is denied by registry permissions or some other external factor. 

</td>
</tr>
</table>
 




## -remarks



Control panel applications can use the registry key opened by this method to store per-type persistent information, such as global configuration parameters. Such private information should be kept in a subkey named <b>OEM</b>; do not store private information in the main type key. Control panel applications can also use this key to read configuration information, such as the strings to use for device calibration prompts. The application should use <b>RegCloseKey</b> to close the registry key. 



