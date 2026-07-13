---
UID: NF:wtsapi32.WTSSetListenerSecurityA
title: WTSSetListenerSecurityA function (wtsapi32.h)
description: Configures the security descriptor of a Remote Desktop Services listener. (ANSI)
helpviewer_keywords: ["WTSSetListenerSecurityA", "WTS_SECURITY_ALL_ACCESS", "WTS_SECURITY_CONNECT", "WTS_SECURITY_CURRENT_GUEST_ACCESS", "WTS_SECURITY_CURRENT_USER_ACCESS", "WTS_SECURITY_DISCONNECT", "WTS_SECURITY_GUEST_ACCESS", "WTS_SECURITY_LOGOFF", "WTS_SECURITY_LOGON", "WTS_SECURITY_MESSAGE", "WTS_SECURITY_QUERY_INFORMATION", "WTS_SECURITY_REMOTE_CONTROL", "WTS_SECURITY_RESET", "WTS_SECURITY_SET_INFORMATION", "WTS_SECURITY_USER_ACCESS", "WTS_SECURITY_VIRTUAL_CHANNELS", "wtsapi32/WTSSetListenerSecurityA"]
old-location: termserv\wtssetlistenersecurity.htm
tech.root: TermServ
ms.assetid: bc90d526-e252-4506-b781-66da5bd66ced
ms.date: 12/05/2018
ms.keywords: WTSSetListenerSecurity, WTSSetListenerSecurity function [Remote Desktop Services], WTSSetListenerSecurityA, WTSSetListenerSecurityW, WTS_SECURITY_ALL_ACCESS, WTS_SECURITY_CONNECT, WTS_SECURITY_CURRENT_GUEST_ACCESS, WTS_SECURITY_CURRENT_USER_ACCESS, WTS_SECURITY_DISCONNECT, WTS_SECURITY_GUEST_ACCESS, WTS_SECURITY_LOGOFF, WTS_SECURITY_LOGON, WTS_SECURITY_MESSAGE, WTS_SECURITY_QUERY_INFORMATION, WTS_SECURITY_REMOTE_CONTROL, WTS_SECURITY_RESET, WTS_SECURITY_SET_INFORMATION, WTS_SECURITY_USER_ACCESS, WTS_SECURITY_VIRTUAL_CHANNELS, termserv.wtssetlistenersecurity, wtsapi32/WTSSetListenerSecurity, wtsapi32/WTSSetListenerSecurityA, wtsapi32/WTSSetListenerSecurityW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSSetListenerSecurityW (Unicode) and WTSSetListenerSecurityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSSetListenerSecurityA
 - wtsapi32/WTSSetListenerSecurityA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSSetListenerSecurity
 - WTSSetListenerSecurityA
 - WTSSetListenerSecurityW
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

A <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that specifies the security information  to set. Always enable the  <b>DACL_SECURITY_INFORMATION</b> and <b>SACL_SECURITY_INFORMATION</b> flags.

For more information about possible values, see <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>.

### -param pSecurityDescriptor [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the security information associated with the listener. For more information about possible values, see <b>SECURITY_DESCRIPTOR</b>. For information about <b>STANDARD_RIGHTS_REQUIRED</b>, see <a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>.


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
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTSSetListenerSecurity as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
