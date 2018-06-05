---
UID: NS:winsock.WSAData
title: WSAData
author: windows-sdk-content
description: Contains information about the Windows Sockets implementation.
old-location: winsock\wsadata_2.htm
old-project: WinSock
ms.assetid: c3c4c0d6-c8b3-4991-bedb-f45816cc8160
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*LPWSADATA, LPWSADATA, LPWSADATA structure pointer [Winsock], WSADATA, WSADATA structure [Winsock], WSAData, _win32_wsadata_2, winsock.wsadata_2, winsock/LPWSADATA, winsock/WSADATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WSADATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winsock.h
api_name:
-	WSADATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAData structure


## -description



			The 
<b>WSADATA</b> structure contains information about the Windows Sockets implementation.


## -struct-fields




### -field wVersion

Type: <b>WORD</b>

The version of the Windows Sockets specification that the <i>Ws2_32.dll</i> expects the caller to use. The high-order byte specifies the minor version number; the low-order byte specifies the major version number.


### -field wHighVersion

Type: <b>WORD</b>

The highest version of the Windows Sockets specification that the <i>Ws2_32.dll</i> can support. The high-order byte specifies the minor version number; the low-order byte specifies the major version number. 

This is the same value as the <b>wVersion</b> member when the version requested in the <i>wVersionRequested</i> parameter passed to the  <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function is the highest version of the Windows Sockets specification that the <i>Ws2_32.dll</i> can support.


### -field szDescription

Type: <b>char[WSADESCRIPTION_LEN+1]</b>

A <b>NULL</b>-terminated ASCII string into which the <i>Ws2_32.dll</i> copies a description of the Windows Sockets implementation. The text (up to 256 characters in length) can contain any characters except control and formatting characters. The most likely use that an application would have for this member is to display it (possibly truncated) in a status message.


### -field szSystemStatus

Type: <b>char[WSASYS_STATUS_LEN+1]</b>

A <b>NULL</b>-terminated ASCII string into which the <i>Ws2_32.dll</i> copies relevant status or configuration information. The <i>Ws2_32.dll</i> should use this parameter only if the information might be useful to the user or support staff. This member should not be considered as an extension of the <b>szDescription</b> parameter.


### -field iMaxSockets

Type: <b>unsigned short</b>

The maximum number of sockets that may be opened. This member should be ignored for Windows Sockets version 2 and later. 

The <b>iMaxSockets</b> member is retained for compatibility with Windows Sockets specification 1.1, but should not be used when developing new applications. No single value can be appropriate for all underlying service providers. The architecture of Windows Sockets changed in version 2 to support multiple providers, and the <b>WSADATA</b> structure no longer applies to a single vendor's stack. 


### -field iMaxUdpDg

Type: <b>unsigned short</b>

The maximum datagram message size. This member is ignored for Windows Sockets version 2 and later. 

The <b>iMaxUdpDg</b> member is retained for compatibility with Windows Sockets specification 1.1, but should not be used when developing new applications. The architecture of Windows Sockets changed in version 2 to support multiple providers, and the <b>WSADATA</b> structure no longer applies to a single vendor's stack. For the actual maximum message size specific to a particular Windows Sockets service provider and socket type, applications should use 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> to retrieve the value of option SO_MAX_MSG_SIZE after a socket has been created.


### -field lpVendorInfo

Type: <b>char FAR*</b>

A pointer to vendor-specific information. This member should be ignored for Windows Sockets version 2 and later. 

The <b>lpVendorInfo</b> member is retained for compatibility with Windows Sockets specification 1.1. The architecture of Windows Sockets changed in version 2 to support multiple providers, and the <b>WSADATA</b> structure no longer applies to a single vendor's stack. Applications needing to access vendor-specific configuration information should use 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> to retrieve the value of option PVD_CONFIG for vendor-specific information. 


## -remarks



The <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function initiates the use of the Windows Sockets DLL by a process.  The <b>WSAStartup</b> function returns a pointer to the  
<b>WSADATA</b> structure in the <i>lpWSAData</i>
parameter.
		

The current version of the Windows Sockets specification returned in the <b>wHighVersion</b> member of the  
<b>WSADATA</b> structure is version 2.2 encoded with the major version number in the low-byte and the minor version number in the high-byte. This version of the current Winsock DLL, <i>Ws2_32.dll</i>, supports applications that request  any of the following  versions of the Windows Sockets specification:<ul>
<li>1.0</li>
<li>1.1</li>
<li>2.0</li>
<li>2.1</li>
<li>2.2</li>
</ul>Depending on the version requested by the application, one of the above version numbers is the value encoded as the major version number in the low-byte and the minor version number in the high-byte that is returned in the <b>wVersion</b> member of the <b>WSADATA</b> structure. 

<div class="alert"><b>Note</b>  An application should ignore the <b>iMaxsockets</b>, <b>iMaxUdpDg</b>, and <b>lpVendorInfo</b> members in <b>WSADATA</b> if the value in <b>wVersion</b> after a successful call to 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> is at least 2. This is because the architecture of Windows Sockets changed in version 2 to support multiple providers, and <b>WSADATA</b> no longer applies to a single vendor's stack. Two new socket options are introduced to supply provider-specific information: SO_MAX_MSG_SIZE (replaces the <b>iMaxUdpDg</b> member) and PVD_CONFIG (allows any other provider-specific configuration to occur).</div>
<div> </div>

#### Examples

The following example demonstrates the use of the <b>WSADATA</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WORD wVersionRequested;
WSADATA wsaData;
int err;
 
wVersionRequested = MAKEWORD( 2, 2 );
 
err = WSAStartup( wVersionRequested, &amp;wsaData );
if ( err != 0 ) {
    /* Tell the user that we could not find a usable */
    /* WinSock DLL.                                  */
    return;
}
 
/* Confirm that the WinSock DLL supports 2.2.*/
/* Note that if the DLL supports versions greater    */
/* than 2.2 in addition to 2.2, it will still return */
/* 2.2 in wVersion since that is the version we      */
/* requested.                                        */
 
if ( LOBYTE( wsaData.wVersion ) != 2 ||
        HIBYTE( wsaData.wVersion ) != 2 ) {
    /* Tell the user that we could not find a usable */
    /* WinSock DLL.                                  */
    WSACleanup( );
    return; 
}
 
/* The WinSock DLL is acceptable. Proceed. */



</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0cd0056e-0c33-4f6e-9f70-5417f8f8da4b">SOL_SOCKET Socket Options</a>



<a href="https://msdn.microsoft.com/6731d27c-fb7d-421a-badf-0cad6a4712ea">Socket Options and IOCTLs</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

