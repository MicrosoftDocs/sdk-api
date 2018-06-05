---
UID: NF:wtsapi32.WTSGetListenerSecurityA
title: WTSGetListenerSecurityA function
author: windows-sdk-content
description: Retrieves the security descriptor of a Remote Desktop Services listener.
old-location: termserv\wtsgetlistenersecurity.htm
old-project: TermServ
ms.assetid: 6e49df9a-679d-4cc1-9297-90cf1e3509fa
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSGetListenerSecurity, WTSGetListenerSecurity function [Remote Desktop Services], WTSGetListenerSecurityA, WTSGetListenerSecurityW, WTS_SECURITY_ALL_ACCESS, WTS_SECURITY_CONNECT, WTS_SECURITY_CURRENT_GUEST_ACCESS, WTS_SECURITY_CURRENT_USER_ACCESS, WTS_SECURITY_DISCONNECT, WTS_SECURITY_GUEST_ACCESS, WTS_SECURITY_LOGOFF, WTS_SECURITY_LOGON, WTS_SECURITY_MESSAGE, WTS_SECURITY_QUERY_INFORMATION, WTS_SECURITY_REMOTE_CONTROL, WTS_SECURITY_RESET, WTS_SECURITY_SET_INFORMATION, WTS_SECURITY_USER_ACCESS, WTS_SECURITY_VIRTUAL_CHANNELS, termserv.wtsgetlistenersecurity, wtsapi32/WTSGetListenerSecurity, wtsapi32/WTSGetListenerSecurityA, wtsapi32/WTSGetListenerSecurityW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSGetListenerSecurityW (Unicode) and WTSGetListenerSecurityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wtsapi32.dll
api_name:
-	WTSGetListenerSecurity
-	WTSGetListenerSecurityA
-	WTSGetListenerSecurityW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSGetListenerSecurityA function


## -description


Retrieves the security descriptor of a Remote Desktop Services listener.


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

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> value that specifies the security information  to retrieve. Always enable the  <b>DACL_SECURITY_INFORMATION</b> and <b>SACL_SECURITY_INFORMATION</b> flags.

For more information about possible values, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>.


### -param pSecurityDescriptor [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that receives the security information associated with  the listener referenced by the <i>pListenerName</i> parameter. The <b>SECURITY_DESCRIPTOR</b> structure is returned in self-relative format. For more information about possible values, see <b>SECURITY_DESCRIPTOR</b>.


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


### -param nLength [in]

The size, in bytes, of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure referenced by the <i>pSecurityDescriptor</i> parameter.


### -param lpnLengthNeeded [out]

A pointer to a variable that receives the number of bytes required to store the complete security descriptor. If this number is less than or equal to the value of the <i>nLength</i> parameter, the security descriptor is copied to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure referenced by the <i>pSecurityDescriptor</i> parameter; otherwise, no action is taken.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



If the number of bytes needed for the buffer that receives the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure is unknown, you can call this method with <i>nLength</i> set to zero. The method will then return, in the <i>lpnLengthNeeded</i> parameter, the number of bytes required for the buffer. Allocate the buffer based on this number, and then call the method again, setting <i>pSecurityDescriptor</i> to the newly allocated buffer and <i>nLength</i> to the number returned by the first call.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
 

 

