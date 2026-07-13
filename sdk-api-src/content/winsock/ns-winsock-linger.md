---
UID: NS:winsock.linger
title: LINGER (winsock.h)
description: The LINGER (winsock.h) structure maintains information about a specific socket that specifies how that socket should behave when data is queued to be sent.
helpviewer_keywords: ["*LPLINGER","*PLINGER","LINGER","_win32_linger_2","linger","linger structure [Winsock]","winsock.linger_2","winsock/linger"]
old-location: winsock\linger_2.htm
tech.root: WinSock
ms.assetid: c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74
ms.date: 08/16/2022
ms.keywords: '*LPLINGER, *PLINGER, LINGER, _win32_linger_2, linger, linger structure [Winsock], winsock.linger_2, winsock/linger'
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINGER, *PLINGER, *LPLINGER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linger
 - winsock/linger
 - PLINGER
 - winsock/PLINGER
 - LINGER
 - winsock/LINGER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsock.h
api_name:
 - linger
---

# LINGER structure


## -description

The 
<b>linger</b> structure maintains information about a specific socket that specifies how that socket should behave when data is queued to be sent and the 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function is called on the socket.

## -struct-fields

### -field l_onoff

Type: <b>u_short</b>

Specifies whether a socket should remain open for a specified amount of time after a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function call to enable queued data to be sent. This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The socket will not remain open. This is the value set if the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function is called with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b> and the <i>optval</i> parameter is zero. 

This value is also set if the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function is called with the <i>optname</i> parameter set to <b>SO_LINGER</b> and the <b>linger</b> structure passed in the <i>optval</i> parameter has the <b>l_onoff</b> member set to 0. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>nonzero</dt>
</dl>
</td>
<td width="60%">
The socket will remain open for a specified amount of time. This value is set if the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function is called with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b> and the <i>optval</i> parameter is nonzero.

This value is also set if the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function is called with the <i>optname</i> parameter set to <b>SO_LINGER</b> and the <b>linger</b> structure passed in the <i>optval</i> parameter has the <b>l_onoff</b> member set to a nonzero value. 

</td>
</tr>
</table>

### -field l_linger

Type: <b>u_short</b>

The linger time in seconds. This member specifies how long to remain open after a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function call to enable queued data to be sent.  This member is only applicable if the <b>l_onoff</b> member of the <b>linger</b> structure is set to a nonzero value.

This value is set if the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function is called with the <i>optname</i> parameter set to <b>SO_LINGER</b>. The <i>optval</i> parameter passed to the <b>setsockopt</b> function must contain a <b>linger</b> structure that is copied to the internal <b>linger</b> structure maintained for the socket.

## -remarks

The <b>l_onoff</b> member of the <b>linger</b> structure determines whether a socket should remain open for a specified amount of time after a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function call to enable queued data to be sent. Somewhat confusing is that this member can be modified in two ways: <ul>
<li>Call the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b>. The <i>optval</i> parameter determines how the <b>l_onoff</b> member is modified. </li>
<li>Call the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_LINGER</b>. The <i>optval</i> parameter specifies how both the <b>l_onoff</b> and <b>l_linger</b> members are modified. </li>
</ul>


The <b>l_linger</b> member of the <b>linger</b> structure determines the amount of time, in seconds, a socket should remain open. This member is only applicable if the <b>l_onoff</b> member of the <b>linger</b> structure is nonzero.

To enable a socket to remain open, an application should set the <b>l_onoff</b> member to a nonzero value and set the <b>l_linger</b> member  to the desired time-out in seconds. To disable a socket from remaining open, an application only needs to set the  <b>l_onoff</b> member of the <b>linger</b> structure to zero.

 If an application calls the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b> to set the <b>l_onoff</b> member to a nonzero value, the value for the <b>l_linger</b> member is not specified. In this case, the time-out used is implementation dependent. If a previous time-out has been established for a socket (by enabling SO_LINGER), this time-out value should be reinstated by the service provider.

Note that enabling a nonzero timeout on a nonblocking socket is not recommended.

The <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function can be called with the <i>optname</i> parameter set to <b>SO_LINGER</b> to retrieve the current value of the <b>linger</b> structure associated with a socket.

## -see-also

<a href="/windows/desktop/WinSock/graceful-shutdown-linger-options-and-socket-closure-2">Graceful Shutdown, Linger Options, and Socket Closure</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>
