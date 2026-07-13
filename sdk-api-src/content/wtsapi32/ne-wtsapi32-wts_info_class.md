---
UID: NE:wtsapi32._WTS_INFO_CLASS
title: WTS_INFO_CLASS (wtsapi32.h)
description: Contains values that indicate the type of session information to retrieve in a call to the WTSQuerySessionInformation function.
helpviewer_keywords: ["WTSApplicationName","WTSClientAddress","WTSClientBuildNumber","WTSClientDirectory","WTSClientDisplay","WTSClientHardwareId","WTSClientInfo","WTSClientName","WTSClientProductId","WTSClientProtocolType","WTSConfigInfo","WTSConnectState","WTSDomainName","WTSIdleTime","WTSIncomingBytes","WTSIncomingFrames","WTSInitialProgram","WTSIsRemoteSession","WTSLogonTime","WTSOEMId","WTSOutgoingBytes","WTSOutgoingFrames","WTSSessionAddressV4","WTSSessionId","WTSSessionInfo","WTSSessionInfoEx","WTSUserName","WTSValidationInfo","WTSWinStationName","WTSWorkingDirectory","WTS_INFO_CLASS","WTS_INFO_CLASS enumeration [Remote Desktop Services]","_win32_wts_info_class_str","termserv.wts_info_class_str","wtsapi32/WTSApplicationName","wtsapi32/WTSClientAddress","wtsapi32/WTSClientBuildNumber","wtsapi32/WTSClientDirectory","wtsapi32/WTSClientDisplay","wtsapi32/WTSClientHardwareId","wtsapi32/WTSClientInfo","wtsapi32/WTSClientName","wtsapi32/WTSClientProductId","wtsapi32/WTSClientProtocolType","wtsapi32/WTSConfigInfo","wtsapi32/WTSConnectState","wtsapi32/WTSDomainName","wtsapi32/WTSIdleTime","wtsapi32/WTSIncomingBytes","wtsapi32/WTSIncomingFrames","wtsapi32/WTSInitialProgram","wtsapi32/WTSIsRemoteSession","wtsapi32/WTSLogonTime","wtsapi32/WTSOEMId","wtsapi32/WTSOutgoingBytes","wtsapi32/WTSOutgoingFrames","wtsapi32/WTSSessionAddressV4","wtsapi32/WTSSessionId","wtsapi32/WTSSessionInfo","wtsapi32/WTSSessionInfoEx","wtsapi32/WTSUserName","wtsapi32/WTSValidationInfo","wtsapi32/WTSWinStationName","wtsapi32/WTSWorkingDirectory","wtsapi32/WTS_INFO_CLASS"]
old-location: termserv\wts_info_class_str.htm
tech.root: TermServ
ms.assetid: 20e015bd-323a-44c4-a0d6-02781f3a5eec
ms.date: 09/03/2025
ms.keywords: WTSApplicationName, WTSClientAddress, WTSClientBuildNumber, WTSClientDirectory, WTSClientDisplay, WTSClientHardwareId, WTSClientInfo, WTSClientName, WTSClientProductId, WTSClientProtocolType, WTSConfigInfo, WTSConnectState, WTSDomainName, WTSIdleTime, WTSIncomingBytes, WTSIncomingFrames, WTSInitialProgram, WTSIsRemoteSession, WTSLogonTime, WTSOEMId, WTSOutgoingBytes, WTSOutgoingFrames, WTSSessionAddressV4, WTSSessionId, WTSSessionInfo, WTSSessionInfoEx, WTSUserName, WTSValidationInfo, WTSWinStationName, WTSWorkingDirectory, WTSCapabilityCheck, WTS_INFO_CLASS, WTS_INFO_CLASS enumeration [Remote Desktop Services], _win32_wts_info_class_str, termserv.wts_info_class_str, wtsapi32/WTSApplicationName, wtsapi32/WTSClientAddress, wtsapi32/WTSClientBuildNumber, wtsapi32/WTSClientDirectory, wtsapi32/WTSClientDisplay, wtsapi32/WTSClientHardwareId, wtsapi32/WTSClientInfo, wtsapi32/WTSClientName, wtsapi32/WTSClientProductId, wtsapi32/WTSClientProtocolType, wtsapi32/WTSConfigInfo, wtsapi32/WTSConnectState, wtsapi32/WTSDomainName, wtsapi32/WTSIdleTime, wtsapi32/WTSIncomingBytes, wtsapi32/WTSIncomingFrames, wtsapi32/WTSInitialProgram, wtsapi32/WTSIsRemoteSession, wtsapi32/WTSLogonTime, wtsapi32/WTSOEMId, wtsapi32/WTSOutgoingBytes, wtsapi32/WTSOutgoingFrames, wtsapi32/WTSSessionAddressV4, wtsapi32/WTSSessionId, wtsapi32/WTSSessionInfo, wtsapi32/WTSSessionInfoEx, wtsapi32/WTSUserName, wtsapi32/WTSValidationInfo, wtsapi32/WTSWinStationName, wtsapi32/WTSWorkingDirectory, wtsapi32/WTS_INFO_CLASS
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTS_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_INFO_CLASS
 - wtsapi32/_WTS_INFO_CLASS
 - WTS_INFO_CLASS
 - wtsapi32/WTS_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_INFO_CLASS
---

# WTS_INFO_CLASS enumeration


## -description

Contains values that indicate the type of 
    session information to retrieve in a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function.

## -enum-fields

### -field WTSInitialProgram

A null-terminated string that contains the name of the initial program that Remote Desktop Services runs when the 
      user logs on.

### -field WTSApplicationName

A null-terminated string that contains the published name of the application that the session is running.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This value is not supported

### -field WTSWorkingDirectory

A null-terminated string that contains the default directory used when launching the initial program.

### -field WTSOEMId

This value is not used.

### -field WTSSessionId

A <b>ULONG</b> value that contains the session identifier.

### -field WTSUserName

A null-terminated string that contains the name of the user associated with the session.

### -field WTSWinStationName

A null-terminated string that contains the name of the Remote Desktop Services session.

<div class="alert"><b>Note</b>  Despite its name, specifying this type does not return the window station name. Rather, it returns the 
       name of the Remote Desktop Services session. Each Remote Desktop Services session is associated with an interactive window 
       station. Because the only supported window station name for an interactive window station is 
       "WinSta0", each session is associated with its own "WinSta0" window station. For more information, see 
      <a href="/windows/desktop/winstation/window-stations">Window Stations</a>.</div>
<div> </div>

### -field WTSDomainName

A null-terminated string that contains the name of the domain to which the logged-on user belongs.

### -field WTSConnectState

The session's current connection state. For more information, see 
      <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a>.

### -field WTSClientBuildNumber

A <b>ULONG</b> value that contains the build number of the client.

### -field WTSClientName

A null-terminated string that contains the name of the client.

### -field WTSClientDirectory

A null-terminated string that contains the directory in which the client is installed.

### -field WTSClientProductId

A <b>USHORT</b> client-specific product identifier.

### -field WTSClientHardwareId

A <b>ULONG</b> value that contains a client-specific hardware identifier. This option is reserved for future use. <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> will always return a value of 0.

### -field WTSClientAddress

The network type and network address of the client. For more information, see 
      <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_address">WTS_CLIENT_ADDRESS</a>.

The IP address is offset by two bytes from the start of the <b>Address</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_address">WTS_CLIENT_ADDRESS</a> 
         structure.

### -field WTSClientDisplay

Information about the display resolution of the client. For more information, see 
      <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a>.

### -field WTSClientProtocolType

A <b>USHORT</b> value that specifies information about the protocol type for the 
      session. This is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
The console session.

</td>
</tr>
<tr>
<td>
1

</td>
<td>
This value is retained for legacy purposes.

</td>
</tr>
<tr>
<td>
2

</td>
<td>
The RDP protocol.

</td>
</tr>
</table>

### -field WTSIdleTime

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

To caculate session idle time, use the <a href="https://learn.microsoft.com/en-us/windows/win32/api/wtsapi32/ns-wtsapi32-wtsinfoa">LastInputTime</a> structure field.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSLogonTime

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSIncomingBytes

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSOutgoingBytes

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSIncomingFrames

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSOutgoingFrames

This value returns <b>FALSE</b>. If you call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information, <b>GetLastError</b> returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not used.

### -field WTSClientInfo

Information about a Remote Desktop Connection (RDC) client. For more information, see <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsclienta">WTSCLIENT</a>.

### -field WTSSessionInfo

Information about a client session on a RD Session Host server. For more information, see <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoa">WTSINFO</a>.

### -field WTSSessionInfoEx

Extended information about a  session on a   RD Session Host server. For more information, see <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoexa">WTSINFOEX</a>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported.

### -field WTSConfigInfo

A <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsconfiginfoa">WTSCONFIGINFO</a> structure that contains information about the configuration of a RD Session Host server.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported.

### -field WTSValidationInfo

This value is not supported.

### -field WTSSessionAddressV4

A <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_address">WTS_SESSION_ADDRESS</a> structure that contains the IPv4 address assigned to the session.
     If the session does not have a virtual IP address, the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function  returns <b>ERROR_NOT_SUPPORTED</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported.

### -field WTSIsRemoteSession

Determines whether the current session is a remote session. The <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function returns a value of <b>TRUE</b> to indicate that the current session is a remote session, and <b>FALSE</b> to indicate that the current session is a local session. This value can only be used for the local machine, so the <i>hServer</i> parameter of the <b>WTSQuerySessionInformation</b> function must contain <b>WTS_CURRENT_SERVER_HANDLE</b>.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported.

### -field WTSSessionActivityId

A **GUID** value that contains the Terminal Services activity ID currently associated with the session.

**Versions prior to Windows Server 2025 or Windows 11 (23H2):** This value is not supported.

### -field WTSCapabilityCheck

An **array of UINT32** values corresponding to whether certain capabilities are supported by the session host.

If the list includes the value `59083637` then that means that RAIL protocol v2 is supported.

**Versions prior to Windows Server 2025 or Windows 11 (24H2):** This value is not supported.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>
