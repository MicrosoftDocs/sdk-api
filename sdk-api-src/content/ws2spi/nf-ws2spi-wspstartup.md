---
UID: NF:ws2spi.WSPStartup
title: WSPStartup function (ws2spi.h)
description: The WSPStartup function initiates use of a Windows Sockets service provider interface (SPI) by a client.
helpviewer_keywords: ["WSPStartup","WSPStartup function [Winsock]","_win32_wspstartup_2","winsock.wspstartup_2","ws2spi/WSPStartup"]
old-location: winsock\wspstartup_2.htm
tech.root: WinSock
ms.assetid: 9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf
ms.date: 12/05/2018
ms.keywords: WSPStartup, WSPStartup function [Winsock], _win32_wspstartup_2, winsock.wspstartup_2, ws2spi/WSPStartup
req.header: ws2spi.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSPStartup
 - ws2spi/WSPStartup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPStartup
---

# WSPStartup function


## -description

The 
**WSPStartup** function initiates use of a Windows Sockets service provider interface  (SPI) by a client.

## -parameters

### -param wVersionRequested [in]

The highest version of Windows Sockets SPI support that the caller can use. The high-order byte specifies the minor version (revision) number; the low-order byte specifies the major version number.

### -param lpWSPData [out]

A pointer to a 
[WSPDATA](ns-ws2spi-wspdata.md) data structure that receives information about the Windows Sockets service provider.

### -param lpProtocolInfo [in]

A pointer to a 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure that defines the characteristics of the desired protocol. This is especially useful when a single provider DLL is capable of instantiating multiple different service providers.

### -param UpcallTable [in]

The Winsock 2 DLL (Ws2_32.dll) upcall dispatch table passed in a [WSPUpCallTable](ns-ws2spi-wspupcalltable.md) structure.

### -param lpProcTable [out]

A pointer to the table of SPI function pointers. This table is returned as an [WSPProc_Table](ns-ws2spi-wspproc_table.md) structure.

## -returns

The 
**WSPStartup** function returns zero if successful. Otherwise, it returns one of the error codes listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSNOTREADY</a></b></dl>
</dl>
</td>
<td width="60%">
Network subsystem is unavailable. 
This error is returned if the Windows Sockets implementation cannot function at this time because the underlying system it uses to provide network services is currently unavailable. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAVERNOTSUPPORTED</a></b></dl>
</dl>
</td>
<td width="60%">
The Winsock.dll version is out of range. This error is returned if the version of Windows Sockets SPI support requested is not provided by this particular Windows Sockets service provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 operation is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROCLIM</a></b></dl>
</dl>
</td>
<td width="60%">
A limit on the number of tasks supported by the Windows Sockets implementation has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpWSPData</i> or <i>lpProcTable</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

Windows Sockets 2  transport service providers are DLLs with a single exported procedure entry point,  **WSPStartup**, used for the service provider initialization function. All other service provider functions are made accessible to the Winsock 2 DLL via the service provider's dispatch table passed in the <i>lpProcTable</i> parameter to the **WSPStartup** function.  Service provider DLL's are loaded into memory by the WinSock 2 DLL only when needed, and are unloaded when their services are no longer required.



The service provider interface also defines several circumstances in which a transport service provider calls up into the Winsock 2 DLL (upcalls) to obtain DLL support services. The transport service provider is returned the upcall dispatch table for the Winsock 2 DLL in the <i>UpcallTable</i> parameter passed to the **WSPStartup** function.


The 
**WSPStartup** function must be the first Windows Sockets SPI function called by a Windows Sockets SPI client on a per-process basis. It allows the client to specify the version of Windows Sockets SPI required and to provide its upcall dispatch table. All upcalls (that is, functions prefixed with WPU) made by the Windows Sockets service provider are invoked through the client's upcall dispatch table. This function also allows the client to retrieve details of the specific Windows Sockets service provider implementation. The Windows Sockets SPI client can only issue further Windows Sockets SPI functions after a successful 
**WSPStartup** invocation. A table of pointers to the rest of the SPI functions is retrieved through the <i>lpProcTable</i> parameter that returns a [WSPProc_Table](ns-ws2spi-wspproc_table.md) structure.

The Winsock 2 DLL loads the service provider's interface DLL into the system by using the standard Windows dynamic library loading mechanisms, and initializes it by calling the **WSPStartup** function. This is usually triggered by an application calling the [socket](/windows/desktop/api/winsock2/nf-winsock2-socket) or [WSASocket](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa) function in order to create a new socket that is to be associated with a service provider whose interface DLL is not currently loaded into memory. 

In order to support future versions of the Windows Sockets SPI and the Ws2_32.dll, which may have functional differences from the current Windows Sockets SPI, a negotiation takes place in 
**WSPStartup**. The caller of 
**WSPStartup** (either the Ws2_32.dll or a layered protocol) and the Windows Sockets service provider indicate to each other the highest version of Windows Sockets that they can support, and each confirms that the other's highest version is acceptable. Upon entry to 
**WSPStartup**, the Windows Sockets service provider examines the version requested by the client. If this version is equal to or higher than the lowest version supported by the service provider, the call succeeds and the service provider returns in the **wHighVersion** member of the [WSPDATA](ns-ws2spi-wspdata.md) structure the highest version it supports and in the **wVersion** member the minimum of its high version and version specified in the <i>wVersionRequested</i> parameter. The Windows Sockets service provider then assumes that the Windows Sockets SPI client will use the version of Windows Sockets specified in the **wVersion** member. If the **wVersion** member of the 
[WSPDATA](ns-ws2spi-wspdata.md) structure is unacceptable to the caller, it should call 
[LPWSPCleanup](nc-ws2spi-lpwspcleanup.md) and either search for another Windows Sockets service provider or fail to initialize.

This negotiation allows both a Windows Sockets service provider and a Windows Sockets SPI client to support a range of Windows Sockets versions. A client can successfully utilize a Windows Sockets service provider if there is any overlap in the version ranges.

The current version of the Windows Sockets specification is version 2.2. The current Winsock DLL, <i>Ws2_32.dll</i>, supports applications that request  any of the following  versions of Windows Sockets specification:  
- 1.0 
- 1.1 
- 2.0 
- 2.1 
- 2.2 
 


To get full access to the new syntax of a higher version of the Windows Sockets specification, the application must negotiate for this higher version. In this case, the <i>wVersionRequested</i> parameter should be set to request version 2.2.  The application must also fully conform to that higher version of the Windows Socket specification, such as compiling against the appropriate header file, linking with a new library, or other special cases. The <i>Winsock2.h header</i> file for Winsock 2 support is included with the Microsoft Windows Software Development Kit (SDK).

Windows Sockets version 2.2 is supported on Windows Server 2008, 
  Windows Vista, Windows Server 2003,
  Windows XP,
  Windows 2000, Windows NT 4.0 with Service Pack 4 (SP4) and later,
  Windows Me,
  Windows 98, and Windows 95 OSR2. 
  Windows Sockets version 2.2 is also supported on   
  Windows 95 with the Windows Socket 2 Update. Applications on these platforms should normally request Winsock 2.2 by setting the <i>wVersionRequested</i> parameter accordingly.

On Windows 95 and versions of Windows NT 3.51 and earlier, Windows Sockets version 1.1 is the highest version of the Windows Sockets specification supported. 

It is legal and possible for an application or DLL written to use a lower version of the Windows Sockets specification that is supported by the Winsock DLL to successfully negotiate this lower version using the  **WSPStartup** function. For example, an application can request version 1.1 in the <i>wVersionRequested</i> parameter passed to the **WSPStartup** function on a platform with the Winsock 2.2 DLL. In this case, the application should only rely on features that fit within the version requested. New Ioctl codes, new behavior of existing functions, and new functions should not be used. The version negotiation provided by the **WSPStartup** was primarily used to allow older Winsock 1.1 applications developed for Windows 95 and   Windows NT 3.51 and earlier to run with the same behavior on later versions of Windows. The <i>Winsock.h header</i> file for Winsock 1.1 support is included with the Windows SDK.

The following chart gives examples of how 
**WSPStartup** works in conjunction with different WS2_32.DLL and Windows Sockets service provider (SP) versions.


<table>
<tr>
<th>DLL<div> </div>versions</th>
<th>SP<div> </div>versions</th>
<th><i>wVersionRequested</i></th>
<th><b>wVersion</b></th>
<th><b>wHighVersion</b></th>
<th>End result</th>
</tr>
<tr>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.0 1.1</td>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>use 1.0</td>
</tr>
<tr>
<td>1.0</td>
<td>1.0 1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>1.1</td>
<td>use 1.0</td>
</tr>
<tr>
<td>1.1</td>
<td>1.0 1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.1</td>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>DLL fails</td>
</tr>
<tr>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>---</td>
<td>---</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAVERNOTSUPPORTED</a></td>
</tr>
<tr>
<td>1.0 1.1</td>
<td>1.0 1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.0 1.1 2.0</td>
<td>1.1</td>
<td>2.0</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.0 1.1 2.0 </td>
<td>2.0</td>
<td>2.0</td>
<td>2.0</td>
<td>2.0</td>
<td>use 2.0</td>
</tr>
<tr>
<td>1.0 1.1 2.0 2.1 2.2</td>
<td>2.2</td>
<td>2.2</td>
<td>2.2</td>
<td>2.2</td>
<td>use 2.2</td>
</tr>
</table>
 



The following code fragment demonstrates how a Windows Sockets SPI client, which supports only version 2 of Windows Sockets SPI, makes a 
**WSPStartup** call:


```cpp
WORD wVersionRequested;
WSPDATA WSPData;
 
int err;
 
WSPUPCALLTABLE upcallTable =
{ 
    /* initialize upcallTable with function pointers */
};
 
LPWSPPROC_TABLE lpProcTable =
{ 
    /* allocate memory for the ProcTable */
};
 
wVersionRequested = MAKEWORD( 2, 2 );
 
err = WSPStartup( wVersionRequested, &WSPData, lpProtocolBuffer, upcallTable, lpProcTable );
if ( err != 0 ) {
    /* Tell the user that we could not find a usable */
    /* Windows Sockets service provider.                     */
    return;
}
 
/* Confirm that the Windows Sockets service provider supports 2.2.*/
/* Note that if the service provider supports versions */
/* greater than 2.2 in addition to 2.2, it will still */
/* return 2.2 in wVersion since that is the version we  */
/* requested.                                           */
 
if ( LOBYTE( WSPData.wVersion ) != 2 ||
         HIBYTE( WSPData.wVersion ) != 2 ) {
    /* Tell the user that we could not find a usable */
    /* Windows Sockets service provider.                     */
    LPWSPCleanup( );
    return;   
}
 
/* The Windows Sockets service provider is acceptable. Proceed. */

```


And this code fragment demonstrates how a Windows Sockets service provider that supports only version 2.2 performs the 
**WSPStartup** negotiation:


```cpp
/* Make sure that the version requested is >= 2.2.  */
/* The low byte is the major version and the high   */
/* byte is the minor version.                       */
 
if ( (LOBYTE( wVersionRequested ) < 2) ||
     ((LOBYTE( wVersionRequested ) == 2) &&
     (HIBYTE( wVersionRequested ) < 2))) {
    return WSAVERNOTSUPPORTED;
}
 
/* Since we only support 2.2, set both wVersion and  */
/* wHighVersion to 2.2.                              */
 
lpWSPData->wVersion = MAKEWORD( 2, 2 );
lpWSPData->wHighVersion = MAKEWORD( 2, 2 );


```


Once the Windows Sockets SPI client has made a successful 
**WSPStartup** call, it can proceed to make other Windows Sockets SPI calls as needed. When it has finished using the services of the Windows Sockets service provider, the client must call 
[LPWSPCleanup](nc-ws2spi-lpwspcleanup.md) in order to allow the Windows Sockets service provider to free any resources allocated for the client.

The **WSPStartup** function must be called at least once by each client process, and may be called multiple times by the Winsock 2 DLL or other entities. A matching [LPWSPCleanup](nc-ws2spi-lpwspcleanup.md) function must be called for each successful **WSPStartup** call.  The service provider should maintain a reference count on a per-process basis.  On each **WSPStartup** call, the caller may specify any version number supported by the service provider DLL.

A service provider must store the pointer to the client's upcall dispatch table that is received as the <i>UpcallTable</i> parameter by the  **WSPStartup** function on a per-process basis.  If a given process calls **WSPStartup** multiple times, the service provider must use only the most recently supplied upcall dispatch table pointer.


A Windows Sockets SPI client can call 
**WSPStartup** more than once if it needs to obtain the 
[WSPDATA](ns-ws2spi-wspdata.md) structure information more than once. On each such call the client can specify any version number supported by the provider.

There must be one 
[LPWSPCleanup](nc-ws2spi-lpwspcleanup.md) call corresponding to every successful 
**WSPStartup** call to allow third-party DLLs to make use of a Windows Sockets provider. This means, for example, that if 
**WSPStartup** is called three times, the corresponding call to 
**LPWSPCleanup** must occur three times. The first two calls to 
**LPWSPCleanup** do nothing except decrement an internal counter; the final 
**LPWSPCleanup** call does all necessary resource deallocation.

This function (and most other service provider functions) can be invoked in a thread that started out as a 16-bit process if the client is a 16-bit Windows Sockets 1.1 client. One important limitation of 16-bit processes is that a 16-bit process cannot create threads. This is significant to service provider implementers that plan to use an internal service thread as part of the implementation.

Fortunately, there are usually only two areas where the conditions for a service thread are strong:

- In the implementation of overlapped I/O completion.
- In the implementation of [LPWSPEventSelect](nc-ws2spi-lpwspeventselect.md).

Both of these areas are only accessible through new Windows Sockets 2 functions, which can only be invoked by 32-bit processes.

A service thread can be safely used if these two design rules are carefully followed:

- Use a service thread only for functionality that is unavailable to 16-bit Windows Sockets 1.1 clients. 
- Create the service thread only on demand. 
 
Several other cautions apply to the use of internal service threads. First, threads generally carry some performance penalty. Use as few as possible, and avoid thread transitions wherever possible. Second, your code should always check for errors in creating threads and fail gracefully and informatively (for example, with 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a>) in case some execution event you did not expect results in a 16-bit process executing a code path that needs threads.

A layered service provider supplies an implementation of this function, but it is also a client of this function when it calls 
**WSPStartup** to initialize the next layer in the protocol chain. The call to the next layer's 
**WSPStartup** may happen during the execution of this layer's 
**WSPStartup** or it may be delayed and called on demand, such as when 
[LPWSPSocket](nc-ws2spi-lpwspsocket.md) is called. In any case, some special considerations apply to this function's <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

The layered provider searches the **ProtocolChain** of the structure referenced by <i>lpProtocolInfo</i> to determine its own location in the chain (by searching for the layer's own catalog entry **Id**) and the identity of the next element in the chain. If the next element is another layer, then, when the next layer's 
**WSPStartup** is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> that references the same unmodified 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
**WSPStartup**. In this case, the base provider's 
**WSAPROTOCOL_INFO** structure should be referenced by the <i>lpProtocolInfo</i> parameter.

One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
**WSAPROTOCOL_INFO** structure through a layered sequence of other functions such as 
[LPWSPAddressToString](nc-ws2spi-lpwspaddresstostring.md), 
[LPWSPDuplicateSocket](nc-ws2spi-lpwspduplicatesocket.md), 
[LPWSPSocket](nc-ws2spi-lpwspsocket.md), or 
[LPWSPStringToAddress](nc-ws2spi-lpwspstringtoaddress.md).

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a>

[LPWSPAddressToString](nc-ws2spi-lpwspaddresstostring.md)

[LPWSPStringToAddress](nc-ws2spi-lpwspstringtoaddress.md)

[LPWSPCleanup](nc-ws2spi-lpwspcleanup.md)

[LPWSPDuplicateSocket](nc-ws2spi-lpwspduplicatesocket.md)

[LPWSPEventSelect](nc-ws2spi-lpwspeventselect.md)

[WSPProc_Table](ns-ws2spi-wspproc_table.md)

[LPWSPSend](nc-ws2spi-lpwspsend.md)

[LPWSPSendTo](nc-ws2spi-lpwspsendto.md)

[LPWSPSocket](nc-ws2spi-lpwspsocket.md)

[WSPUpCallTable](ns-ws2spi-wspupcalltable.md)

