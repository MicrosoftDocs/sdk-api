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

# WTSSetListenerSecurityA function


## -description


Configures the security descriptor of a Remote Desktop Services listener.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.


### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.


### -param pListenerName [in]

A pointer to a null-terminated string that contains the name of the listener.


### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> value that specifies the security information  to set. Always enable the  <b>DACL_SECURITY_INFORMATION</b> and <b>SACL_SECURITY_INFORMATION</b> flags.

For more information about possible values, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>.


### -param pSecurityDescriptor [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that contains the security information associated with the listener. For more information about possible values, see <b>SECURITY_DESCRIPTOR</b>. For information about <b>STANDARD_RIGHTS_REQUIRED</b>, see <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.


The discretionary access control list (DACL) of the security descriptor can contain one or more of the following values.





#### WTS_SECURITY_ALL_ACCESS

Combines these values:

<ul>
<li><b>STANDARD_RIGHTS_REQUIRED</b></li>
<li><b>WTS_SECURITY_CONNECT</b></li>
<li><b>WTS_SECURITY_DISCONNECT</b></li>
<li><b>WTS_SECURITY_LOGON</b></li>
<li><b>WTS_SECURITY_MESSAGE</b></li>
<li><b>WTS_SECURITY_QUERY_INFORMATION</b></li>
<li><b>WTS_SECURITY_REMOTE_CONTROL</b></li>
<li><b>WTS_SECURITY_RESET</b></li>
<li><b>WTS_SECURITY_SET_INFORMATION</b></li>
<li><b>WTS_SECURITY_VIRTUAL_CHANNELS</b></li>
</ul>


#### WTS_SECURITY_CONNECT (256 (0x100))

The right to connect.



#### WTS_SECURITY_CURRENT_GUEST_ACCESS

Combines these values:

<ul>
<li><b>WTS_SECURITY_LOGOFF</b></li>
<li><b>WTS_SECURITY_VIRTUAL_CHANNELS</b></li>
</ul>


#### WTS_SECURITY_CURRENT_USER_ACCESS

Combines these values:

<ul>
<li><b>WTS_SECURITY_DISCONNECT</b></li>
<li><b>WTS_SECURITY_LOGOFF</b></li>
<li><b>WTS_SECURITY_RESET</b></li>
<li><b>WTS_SECURITY_SET_INFORMATION</b></li>
<li><b>WTS_SECURITY_VIRTUAL_CHANNELS</b></li>
</ul>


#### WTS_SECURITY_DISCONNECT (512 (0x200))

The right to disconnect.



#### WTS_SECURITY_GUEST_ACCESS

Defined as <b>WTS_SECURITY_LOGON</b>.



#### WTS_SECURITY_LOGOFF (64 (0x40))

The right to log off.



#### WTS_SECURITY_LOGON (32 (0x20))

The right to log on.



#### WTS_SECURITY_MESSAGE (128 (0x80))

The right to send a message to the user.



#### WTS_SECURITY_QUERY_INFORMATION (1 (0x1))

The right to  query for information.



#### WTS_SECURITY_REMOTE_CONTROL (16 (0x10))

The right to use remote control.



#### WTS_SECURITY_RESET (4 (0x4))

The right to  reset information.



#### WTS_SECURITY_SET_INFORMATION (2 (0x2))

The right to  set information.



#### WTS_SECURITY_USER_ACCESS

Combines these values:

<ul>
<li><b>WTS_SECURITY_CONNECT</b></li>
<li><b>WTS_SECURITY_CURRENT_GUEST_ACCESS</b></li>
<li><b>WTS_SECURITY_QUERY_INFORMATION</b></li>
</ul>


#### WTS_SECURITY_VIRTUAL_CHANNELS (8 (0x8))

The right to use virtual channels.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
 

 

