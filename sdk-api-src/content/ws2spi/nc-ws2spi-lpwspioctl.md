---
UID: NC:ws2spi.LPWSPIOCTL
title: LPWSPIOCTL
description: The LPWSPIoctl function controls the mode of a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPIOCTL"]
ms.date: 08/16/2022
ms.keywords: LPWSPIOCTL
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPIOCTL
f1_keywords:
 - LPWSPIOCTL
 - ws2spi/LPWSPIOCTL
---

## -description

The **LPWSPIoctl** function controls the mode of a socket.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param dwIoControlCode [in]

The control code of the operation to perform.

### -param lpvInBuffer [in]

A pointer to the input buffer.

### -param cbInBuffer [in]

The size, in bytes, of the input buffer.

### -param lpvOutBuffer [out]

A pointer to the output buffer.

### -param cbOutBuffer [in]

The size, in bytes, of the output buffer.

### -param lpcbBytesReturned [out]

A pointer to actual number of bytes of output.

### -param lpOverlapped [in]

A pointer to a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure (ignored for non-overlapped sockets).

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](../winsock2/nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets). See Remarks.

### -param lpThreadId [in]

A pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure to be used by the provider in a subsequent call to <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. The provider should store the referenced **WSATHREADID** structure (not the pointer) until after the **WPUQueueApc** function returns.

### -param lpErrno [in]

A pointer to the error code.

## -returns

If no error occurs and the operation has completed immediately, **LPWSPIoctl** returns zero. Note that in this case the completion routine, if specified, will have already been queued. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>. The error code WSA_IO_PENDING indicates that an overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that no overlapped operation was initiated and no completion indication will occur.

| Error code                                                                                                                                          | Meaning                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WSA_IO_PENDING](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-io-pending)     | An overlapped operation was successfully initiated and completion will be indicated at a later time.                                                                                                                                                                     |
| [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault)               | The <i>lpvInBuffer</i>, <i>lpvOutBuffer</i> or <i>lpcbBytesReturned</i> parameter is not totally contained in a valid part of the user address space, or the *cbInBuffer* or <i>cbOutBuffer</i> parameter is too small.                                                  |
| [WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)               | The <i>dwIoControlCode</i> is not a valid command, or a supplied input parameter is not acceptable, or the command is not applicable to the type of socket supplied.                                                                                                     |
| [WSAEINPROGRESS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinprogress)     | The function is invoked when a callback is in progress.                                                                                                                                                                                                                  |
| [WSAENETDOWN](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenetdown)           | The network subsystem has failed.                                                                                                                                                                                                                                        |
| [WSAENOTSOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenotsock)           | The descriptor <i>s</i> is not a socket.                                                                                                                                                                                                                                 |
| [WSAEOPNOTSUPP](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeopnotsupp)       | The specified IOCTL command cannot be realized. For example, the flow specifications specified in **SIO_SET_QOS** cannot be satisfied.                                                                                                                                   |
| [WSAEWOULDBLOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaewouldblock)     | The socket is marked as nonblocking and the requested operation would block.

## -remarks

This routine is used to set or retrieve operating parameters associated with the socket, the transport protocol, or the communications subsystem. If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are **NULL**, the socket in this function will be treated as a nonoverlapped socket.

For non-overlapped sockets, <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters are ignored and this function can block if socket <i>s</i> is in blocking mode. Note that if socket <i>s</i> is in nonblocking mode, this function can return [WSAEWOULDBLOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaewouldblock) if the specified operation cannot be finished immediately. In this case, the Windows Sockets SPI client may change the socket to blocking mode and reissue the request or wait for the corresponding network event (such as FD_ROUTING_INTERFACE_CHANGE or FD_ADDRESS_LIST_CHANGE in case of **SIO_ROUTING_INTERFACE_CHANGE** or **SIO_ADDRESS_LIST_CHANGE**) using Windows message (through **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** or event (using [**LPWSPEventSelect**](./nc-ws2spi-lpwspeventselect.md)) based notification mechanism.

For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time. The **DWORD** value pointed to by the <i>lpcbBytesReturned</i> parameter that is returned may be ignored. The final completion status and bytes returned can be retrieved when the appropriate completion method is signaled when the operation has completed.

Any IOCTL may block indefinitely, depending on the implementation of the service provider. If the Windows Sockets SPI client cannot tolerate blocking in a **LPWSPIoctl** call, overlapped I/O would be advised for IOCTLs that are most likely to block including:

-   **SIO_ADDRESS_LIST_CHANGE**
-   **SIO_FINDROUTE**
-   **SIO_FLUSH**
-   **SIO_GET_QOS**
-   **SIO_GET_GROUP_QOS**
-   **SIO_ROUTING_INTERFACE_CHANGE**
-   **SIO_SET_QOS**
-   **SIO_SET_GROUP_QOS**

Some protocol-specific IOCTLs may also be particularly likely to block. Check the relevant protocol-specific annex for available information.

The prototype for the completion routine pointed to by the <i>lpCompletionRoutine</i> parameter is as follows.

```cpp
void CALLBACK 
CompletionRoutine(  
  IN DWORD           dwError, 
  IN DWORD           cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD           dwFlags 
);
```

The CompletionRoutine is a placeholder for an application-supplied function name. The <i>dwError</i> parameter specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i> parameter. The <i>cbTransferred</i> parameter specifies the number of bytes received. The <i>dwFlags</i> parameter is not used for this IOCTL. The completion routine does not return a value.

In as much as the <i>dwIoControlCode</i> parameter is now a 32-bit entity, it is possible to adopt an encoding scheme that provides a convenient way to partition the opcode identifier space. The <i>dwIoControlCode</i> parameter is constructed to allow for protocol and vendor independence when adding new control codes, while retaining backward compatibility with Windows Sockets 1.1 and UNIX control codes. The <i>dwIoControlCode</i> parameter has the following form.


| bit 31 | bit 30 | bit 29 | bits 28 and 27 | bits 26 thru 16 | bits 15 thru 0 |
|----|----|----|-----|-----------------------|---------------------------------|
| I | O | V | T | Vendor/Address family | Code |

**I** is set if the input buffer is valid for the code, as with **IOC_IN**.

**O** is set if the output buffer is valid for the code, as with **IOC_OUT**. Note that for codes with both input and output parameters, both **I** and **O** will be set.

**V** is set if there are no parameters for the code, as with **IOC_VOID**.

**T** is a two-bit quantity that defines the type of IOCTL. The following values are defined.
- **0** indicates that the IOCTL is a standard UNIX IOCTL code, as with **FIONREAD**, **FIONBIO**, and so on.
- **1** indicates that the IOCTL is a generic Windows Sockets 2 IOCTL code. New IOCTL codes defined for Windows Sockets 2 will have **T** == **1**.
- **2** indicates that the IOCTL applies only to a specific address family.
- **3**  The IOCTL applies only to a specific vendor's provider. This type allows companies to be assigned a vendor number that appears in the **Vendor/Address family** member. Then, the vendor can define new IOCTLs specific to that vendor without having to register the IOCTL with a clearinghouse, thereby providing vendor flexibility and privacy.

**Vendor/Address family** is an 11-bit quantity that defines the vendor who owns the code (if **T** == **3**), or that contains the address family to which the code applies (if **T** == **2**). If this is a UNIX IOCTL code (**T** == **0**) then this member has the same value as the code on UNIX. If this is a generic Windows Sockets 2 IOCTL (**T** == **1**) then this member can be used as an extension of the code member to provide additional code values.

**Code** is the specific IOCTL code for the operation.

The following UNIX commands are supported:

<dl> <dt>

<span id="FIONBIO"></span><span id="fionbio"></span>**FIONBIO**
</dt> <dd>

Enables or disables nonblocking mode on socket <i>s</i>. The <i>lpvInBuffer</i> parameter points at an unsigned long, which is nonzero if nonblocking mode is to be enabled and zero if it is to be disabled. When a socket is created, it operates in blocking mode (that is, nonblocking mode is disabled). This is consistent with Berkeley Software Distribution (BSD) sockets.

The **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** or [**LPWSPEventSelect**](./nc-ws2spi-lpwspeventselect.md) routine automatically sets a socket to nonblocking mode. If **LPWSPAsyncSelect** or **LPWSPEventSelect** has been issued on a socket, then any attempt to use **LPWSPIoctl** to set the socket back to blocking mode will fail with [WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval). To set the socket back to blocking mode, a Windows Sockets SPI client must first disable **LPWSPAsyncSelect** by calling **LPWSPAsyncSelect** with the *lEvent* parameter equal to zero, or disable **LPWSPEventSelect** by calling **LPWSPEventSelect** with the *lNetworkEvents* parameter equal to zero.

</dd> <dt>

<span id="FIONREAD"></span><span id="fionread"></span>**FIONREAD**
</dt> <dd>

Determine the amount of data that can be read atomically from socket <i>s</i>. The <i>lpvOutBuffer</i> parameter points at an **unsigned long** in which [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) stores the result.

If the socket passed in the <i>s</i> parameter is stream oriented (for example, type SOCK_STREAM), **FIONREAD** returns the total amount of data that can be read in a single receive operation; this is normally the same as the total amount of data queued on the socket (since a data stream is byte-oriented, this is not guaranteed).

If the socket passed in the <i>s</i> parameter is message oriented (for example, type SOCK_DGRAM), **FIONREAD** returns the reports the total number of bytes available to read, not the size of the first datagram (message) queued on the socket.

</dd> <dt>

<span id="SIOCATMARK"></span><span id="siocatmark"></span>**SIOCATMARK**
</dt> <dd>

Determines whether or not all OOB data has been read. This applies only to a socket of stream style (for example, type SOCK_STREAM) that has been configured for inline reception of any OOB data (SO_OOBINLINE). If no OOB data is waiting to be read, the operation returns **TRUE**. Otherwise, it returns **FALSE**, and the next receive operation performed on the socket will retrieve some or all of the data preceding the mark; the Windows Sockets SPI client should use the **SIOCATMARK** operation to determine whether any remains. If there is any normal data preceding the urgent (OOB) data, it will be received in order. (Note that receive operations will never mix OOB and normal data in the same call.) <i>lpvOutBuffer</i> points at a **BOOL** in which **LPWSPIoctl** stores the result.

</dd> </dl>

The following Windows Sockets 2 commands are supported:

<dl> <dt>

<span id="SIO_ACQUIRE_PORT_RESERVATION__opcode_setting__I__T__3_"></span><span id="sio_acquire_port_reservation__opcode_setting__i__t__3_"></span><span id="SIO_ACQUIRE_PORT_RESERVATION__OPCODE_SETTING__I__T__3_"></span>**SIO_ACQUIRE_PORT_RESERVATION** (opcode setting: I, T==3)
</dt> <dd>

Request a runtime reservation for a block of TCP or UDP ports. For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted. Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](/windows/win32/winsock/sio-acquire-port-reservation) IOCTL was called. In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](../iphlpapi/nf-iphlpapi-createpersistenttcpportreservation.md) or [**CreatePersistentUdpPortReservation**](../iphlpapi/nf-iphlpapi-createpersistentudpportreservation.md) function may be consumed by any process with the ability to obtain persistent reservations.

For more detailed information, see the [**SIO_ACQUIRE_PORT_RESERVATION**](/windows/win32/winsock/sio-acquire-port-reservation) reference.

[**SIO_ACQUIRE_PORT_RESERVATION**](/windows/win32/winsock/sio-acquire-port-reservation) is supported on Windows Vista and later versions of the operating system.

</dd> <dt>

<span id="SIO_ADDRESS_LIST_CHANGE__opcode_setting__T__1_"></span><span id="sio_address_list_change__opcode_setting__t__1_"></span><span id="SIO_ADDRESS_LIST_CHANGE__OPCODE_SETTING__T__1_"></span>**SIO_ADDRESS_LIST_CHANGE** (opcode setting: T==1)
</dt> <dd>

To receive notification of changes in the list of local transport addresses of the socket's protocol family to which the Windows Sockets SPI client can bind. No output information will be provided upon completion of this IOCTL; the completion merely indicates that the list of available local addresses has changed and should be queried again through **SIO_ADDRESS_LIST_QUERY**.

It is assumed (although not required) that the Windows Sockets SPI client uses overlapped I/O to be notified of change by completion of **SIO_ADDRESS_LIST_CHANGE** request. Alternatively, if the **SIO_ADDRESS_LIST_CHANGE** IOCTL is issued on a nonblocking socket and without overlapped parameters (<i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are set to **NULL**), it will complete immediately with error [WSAEWOULDBLOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaewouldblock). The Windows Sockets SPI client can then wait for address list change events through a call to [**LPWSPEventSelect**](./nc-ws2spi-lpwspeventselect.md) or **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** with the FD_ADDRESS_LIST_CHANGE bit set in the network event bitmask.

</dd> <dt>

<span id="SIO_ADDRESS_LIST_QUERY__opcode_setting___O__T__1_"></span><span id="sio_address_list_query__opcode_setting___o__t__1_"></span><span id="SIO_ADDRESS_LIST_QUERY__OPCODE_SETTING___O__T__1_"></span>**SIO_ADDRESS_LIST_QUERY** (opcode setting: O, T==1)
</dt> <dd>

Obtains a list of local transport addresses of the socket's protocol family to which the application can bind. The list of addresses varies based on address family and some addresses are excluded from the list.

> [!Note]  
> In Windows Plug-n-Play environments, addresses can be added and removed dynamically. Therefore, applications cannot rely on the information returned by **SIO_ADDRESS_LIST_QUERY** to be persistent. Applications may register for address change notifications through the **SIO_ADDRESS_LIST_CHANGE** IOCTL which provides for notification through either overlapped I/O or FD_ADDRESS_LIST_CHANGE event. The following sequence of actions can be used to guarantee that the application always has current address list information:

 

-   Issue **SIO_ADDRESS_LIST_CHANGE** IOCTL
-   Issue **SIO_ADDRESS_LIST_QUERY** IOCTL
-   Whenever **SIO_ADDRESS_LIST_CHANGE** IOCTL notifies the application of address list change (either through overlapped I/O or by signaling FD_ADDRESS_LIST_CHANGE event), the whole sequence of actions should be repeated.

For more detailed information, see the [**SIO_ADDRESS_LIST_QUERY**](/windows/win32/winsock/sio-address-list-query) reference. **SIO_ADDRESS_LIST_QUERY** is supported on Windows 2000 and later.

</dd> <dt>

<span id="SIO_ASSOCIATE_HANDLE__opcode_setting__I__T__1_"></span><span id="sio_associate_handle__opcode_setting__i__t__1_"></span><span id="SIO_ASSOCIATE_HANDLE__OPCODE_SETTING__I__T__1_"></span>**SIO_ASSOCIATE_HANDLE** (opcode setting: I, T==1)
</dt> <dd>

Associates this socket with the specified handle of a companion interface. The input buffer contains the integer value corresponding to the manifest constant for the companion interface (for example, TH_NETDEV and TH_TAPI), followed by a value that is a handle of the specified companion interface, along with any other required information. Refer to the appropriate section in the <i>Windows Sockets 2 Protocol-Specific Annex</i> and/or documentation for the particular companion interface for additional details. (These resources may only be available in English.) The total size is reflected in the input buffer length. No output buffer is required. The <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a>  error code is indicated for service providers that do not support this IOCTL. The handle associated by this IOCTL can be retrieved using **SIO_TRANSLATE_HANDLE**.

A companion interface might be used, for example, if a particular provider provides:

-   A great deal of additional control over the behavior of a socket.
-   Provider-specific controls that do not map to existing Windows Socket functions (or those likely for the future).

It is recommended that the Component Object Model (COM) be used instead of this IOCTL to discover and track other interfaces that might be supported by a socket. This IOCTL is present for backward compatibility with systems where COM is not available or cannot be used for some other reason.

</dd> <dt>

<span id="SIO_ASSOCIATE_PORT_RESERVATION__opcode_setting__I__T__3_"></span><span id="sio_associate_port_reservation__opcode_setting__i__t__3_"></span><span id="SIO_ASSOCIATE_PORT_RESERVATION__OPCODE_SETTING__I__T__3_"></span>**SIO_ASSOCIATE_PORT_RESERVATION** (opcode setting: I, T==3)
</dt> <dd>

Associate a socket with a persistent or runtime reservation for a block of TCP or UDP ports identified by the port reservation token. The [**SIO_ASSOCIATE_PORT_RESERVATION**](/windows/win32/winsock/sio-associate-port-reservation) IOCTL must be issued before the socket is bound. If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token. If no ports are available from the specified reservation, the <b><a href="/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b> function call will fail.

For more detailed information, see the [**SIO_ASSOCIATE_PORT_RESERVATION**](/windows/win32/winsock/sio-associate-port-reservation) reference.

[**SIO_ASSOCIATE_PORT_RESERVATION**](/windows/win32/winsock/sio-associate-port-reservation) is supported on Windows Vista and later versions of the operating system.

</dd> <dt>

<span id="SIO_BASE_HANDLE__opcode_setting__O__T__1_"></span><span id="sio_base_handle__opcode_setting__o__t__1_"></span><span id="SIO_BASE_HANDLE__OPCODE_SETTING__O__T__1_"></span>**SIO_BASE_HANDLE** (opcode setting: O, T==1)
</dt> <dd>

Retrieves the base service provider handle for a given socket. The returned value is a **SOCKET**.

A layered service provider should never intercept this IOCTL since the return value must be the socket handle from the base service provider.

If the output buffer is not large enough for a socket handle (the <i>cbOutBuffer</i> is less than the size of a **SOCKET**) or the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault).

**SIO_BASE_HANDLE** is defined in the <i>Mswsock.h</i> header file and supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_BSP_HANDLE__opcode_setting__O__T__1_"></span><span id="sio_bsp_handle__opcode_setting__o__t__1_"></span><span id="SIO_BSP_HANDLE__OPCODE_SETTING__O__T__1_"></span>**SIO_BSP_HANDLE** (opcode setting: O, T==1)
</dt> <dd>

Retrieves the base service provider handle for a socket used by the [**WSASendMsg**](../winsock2/nf-winsock2-wsasendmsg.md) function. The returned value is a **SOCKET**.

This Ioctl is used by a layered service provider to ensure the provider intercept the [**WSASendMsg**](../winsock2/nf-winsock2-wsasendmsg.md) function.


If the output buffer is not large enough for a socket handle (the <i>cbOutBuffer</i> is less than the size of a **SOCKET**) or the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault).

**SIO_BSP_HANDLE** is defined in the <i>Mswsock.h</i> header file and supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_BSP_HANDLE_SELECT__opcode_setting__O__T__1_"></span><span id="sio_bsp_handle_select__opcode_setting__o__t__1_"></span><span id="SIO_BSP_HANDLE_SELECT__OPCODE_SETTING__O__T__1_"></span>**SIO_BSP_HANDLE_SELECT** (opcode setting: O, T==1)
</dt> <dd>

Retrieves the base service provider handle for a socket used by the [**select**](/sql/t-sql/queries/select-transact-sql) function. The returned value is a **SOCKET**.

This Ioctl is used by a layered service provider to ensure the provider intercept the [**select**](/sql/t-sql/queries/select-transact-sql) function.

If the output buffer is not large enough for a socket handle (the <i>cbOutBuffer</i> is less than the size of a **SOCKET**) or the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault).

**SIO_BSP_HANDLE_SELECT** is defined in the <i>Mswsock.h</i> header file and supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_BSP_HANDLE_POLL__opcode_setting__O__T__1_"></span><span id="sio_bsp_handle_poll__opcode_setting__o__t__1_"></span><span id="SIO_BSP_HANDLE_POLL__OPCODE_SETTING__O__T__1_"></span>**SIO_BSP_HANDLE_POLL** (opcode setting: O, T==1)
</dt> <dd>

Retrieves the base service provider handle for a socket used by the [**WSAPoll**](../winsock2/nf-winsock2-wsapoll.md) function. The <i>lpOverlapped</i> parameter must be a **NULL** pointer. The returned value is a **SOCKET**.

This Ioctl is used by a layered service provider to ensure the provider intercept the [**WSAPoll**](../winsock2/nf-winsock2-wsapoll.md) function.

If the output buffer is not large enough for a socket handle (the <i>cbOutBuffer</i> is less than the size of a **SOCKET**), the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, or the <i>lpOverlapped</i> parameter is not a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault).

**SIO_BSP_HANDLE_POLL** is defined in the <i>Mswsock.h</i> header file and supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_CHK_QOS__opcode_setting__I__O__T__3_"></span><span id="sio_chk_qos__opcode_setting__i__o__t__3_"></span><span id="SIO_CHK_QOS__OPCODE_SETTING__I__O__T__3_"></span>**SIO_CHK_QOS** (opcode setting: I, O, T==3)
</dt> <dd>


Retrieves information about QoS traffic characteristics. During the transitional phase on the sending system between flow setup and the receipt of a RESV message (see How the RSVP Service Invokes TC for more information on the transitional phase), traffic associated with an RSVP flow is shaped based on service type ( BEST EFFORT, CONTROLLED LOAD, or [GUARANTEED](/windows/win32/winsock/guarantee-2)). For more information, see Using SIO_CHK_QOS in the Quality of Service section of the Platform Software Development Kit (SDK).

</dd> <dt>

<span id="SIO_ENABLE_CIRCULAR_QUEUEING__opcode_setting__V__T__1_"></span><span id="sio_enable_circular_queueing__opcode_setting__v__t__1_"></span><span id="SIO_ENABLE_CIRCULAR_QUEUEING__OPCODE_SETTING__V__T__1_"></span>**SIO_ENABLE_CIRCULAR_QUEUEING** (opcode setting: V, T==1)
</dt> <dd>

Indicates to a message-oriented service provider that a newly arrived message should never be dropped because of a buffer queue overflow. Instead, the oldest message in the queue should be eliminated in order to accommodate the newly arrived message. No input and output buffers are required. Note that this IOCTL is only valid for sockets associated with unreliable, message-oriented protocols. The WSAENOPROTOOPT error code is indicated for service providers that do not support this IOCTL.

</dd> <dt>

<span id="SIO_FIND_ROUTE__opcode_setting__O__T__1_"></span><span id="sio_find_route__opcode_setting__o__t__1_"></span><span id="SIO_FIND_ROUTE__OPCODE_SETTING__O__T__1_"></span>**SIO_FIND_ROUTE** (opcode setting: O, T==1)
</dt> <dd>

When issued, this IOCTL requests that the route to the remote address specified as a <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> in the input buffer be discovered. If the address already exists in the local cache, its entry is invalidated. In the case of Novell's IPX, this call initiates an IPX GetLocalTarget (GLT), that queries the network for the given remote address.

</dd> <dt>

<span id="SIO_FLUSH__opcode_setting__V__T__1_"></span><span id="sio_flush__opcode_setting__v__t__1_"></span><span id="SIO_FLUSH__OPCODE_SETTING__V__T__1_"></span>**SIO_FLUSH** (opcode setting: V, T==1)
</dt> <dd>

Discards current contents of the sending queue associated with this socket. No input and output buffers are required. The <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a>  error code is indicated for service providers that do not support this IOCTL.

</dd> <dt>

<span id="SIO_GET_BROADCAST_ADDRESS__opcode_setting__O__T__1_"></span><span id="sio_get_broadcast_address__opcode_setting__o__t__1_"></span><span id="SIO_GET_BROADCAST_ADDRESS__OPCODE_SETTING__O__T__1_"></span>**SIO_GET_BROADCAST_ADDRESS** (opcode setting: O, T==1)
</dt> <dd>

This IOCTL fills the output buffer with a <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> structure containing a suitable broadcast address for use with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b>.

</dd> <dt>

<span id="SIO_GET_EXTENSION_FUNCTION_POINTER__opcode_setting__O__I__T__1_"></span><span id="sio_get_extension_function_pointer__opcode_setting__o__i__t__1_"></span><span id="SIO_GET_EXTENSION_FUNCTION_POINTER__OPCODE_SETTING__O__I__T__1_"></span>**SIO_GET_EXTENSION_FUNCTION_POINTER** (opcode setting: O, I, T==1)
</dt> <dd>

Retrieve a pointer to the specified extension function supported by the associated service provider. The input buffer contains a globally unique identifier (**GUID**) whose value identifies the extension function in question. The pointer to the desired function is returned in the output buffer. Extension function identifiers are established by service provider vendors and should be included in vendor documentation that describes extension function capabilities and semantics.

The GUID values for extension functions supported by the Windows TCP/IP service provider are defined in the <i>Mswsock.h</i> header file. The possible value for these GUIDs are as follows:



| Term                                                                                                                             | Description                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID_ACCEPTEX<br/>                                     | The [**AcceptEx**](../mswsock/nf-mswsock-acceptex.md) extension function.<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID_CONNECTEX<br/>                                  | The [**ConnectEx**](../mswsock/nc-mswsock-lpfn_connectex.md) extension function.<br/>                       |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID_DISCONNECTEX<br/>                         | The [**DisconnectEx**](../mswsock/nc-mswsock-lpfn_disconnectex.md) extension function. <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID_GETACCEPTEXSOCKADDRS<br/> | The [**GetAcceptExSockaddrs**](../mswsock/nf-mswsock-getacceptexsockaddrs.md) extension function.<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>WSAID_TRANSMITFILE<br/>                         | The [**TransmitFile**](../mswsock/nf-mswsock-transmitfile.md) extension function.<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>WSAID_TRANSMITPACKETS<br/>                | The [**TransmitPackets**](../mswsock/nc-mswsock-lpfn_transmitpackets.md) extension function.<br/>           |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID_WSARECVMSG<br/>                               | The [**LPFN_WSARECVMSG (WSARecvMsg)**](../mswsock/nc-mswsock-lpfn_wsarecvmsg.md) extension function.<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID_WSASENDMSG<br/>                               | The [**WSASendMsg**](../winsock2/nf-winsock2-wsasendmsg.md) extension function. <br/>                      |



 

</dd> <dt>

<span id="SIO_GET_GROUP_QOS__opcode_setting__O__T__1_"></span><span id="sio_get_group_qos__opcode_setting__o__t__1_"></span><span id="SIO_GET_GROUP_QOS__OPCODE_SETTING__O__T__1_"></span>**SIO_GET_GROUP_QOS** (opcode setting: O, T==1)
</dt> <dd>

Reserved.

</dd> <dt>

<span id="SIO_GET_INTERFACE_LIST__opcode_setting__O__T__0_"></span><span id="sio_get_interface_list__opcode_setting__o__t__0_"></span><span id="SIO_GET_INTERFACE_LIST__OPCODE_SETTING__O__T__0_"></span>**SIO_GET_INTERFACE_LIST** (opcode setting: O, T==0)
</dt> <dd>


Returns a list of configured IP interfaces and their parameters as an array of [**INTERFACE_INFO**](../ws2ipdef/ns-ws2ipdef-interface_info.md) structures.

> [!Note]  
> Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.

 


The <i>lpvOutBuffer</i> parameter points to the buffer in which to store the information about interfaces as an array of [**INTERFACE_INFO**](../ws2ipdef/ns-ws2ipdef-interface_info.md) structures for unicast IP addresses on the interfaces. The <i>cbOutBuffer</i> parameter specifies the length of the output buffer. The number of interfaces returned (number of structures returned in the buffer pointed to by <i>lpvOutBuffer</i> parameter) can be determined based on the actual length of the output buffer returned in <i>lpcbBytesReturned</i> parameter.

If the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function is called with **SIO_GET_INTERFACE_LIST** and the level member of the socket <i>s</i> parameter is not defined as **IPPROTO_IP**, **WSAEINVAL** is returned. A call to the **WSAIoctl** function with **SIO_GET_INTERFACE_LIST** returns **WSAEFAULT** if the <i>cbOutBuffer</i> parameter that specifies the length of the output buffer is too small ro receive the list of configured interfaces.

</dd> <dt>

<span id="SIO_GET_INTERFACE_LIST_EX__opcode_setting__O__T__0_"></span><span id="sio_get_interface_list_ex__opcode_setting__o__t__0_"></span><span id="SIO_GET_INTERFACE_LIST_EX__OPCODE_SETTING__O__T__0_"></span>**SIO_GET_INTERFACE_LIST_EX** (opcode setting: O, T==0)
</dt> <dd>

Reserved for future use with sockets.

Returns a list of configured IP interfaces and their parameters as an array of [**INTERFACE_INFO_EX**](../ws2ipdef/ns-ws2ipdef-interface_info_ex.md) structures.

The <i>lpvOutBuffer</i> parameter points to the buffer in which to store the information about interfaces as an array of [**INTERFACE_INFO_EX**](../ws2ipdef/ns-ws2ipdef-interface_info_ex.md) structures for unicast IP addresses on the interface. The <i>cbOutBuffer</i> parameter specifies the length of the output buffer. The number of interfaces returned (number of structures returned in <i>lpvOutBuffer</i>) can be determined based on the actual length of the output buffer returned in <i>lpcbBytesReturned</i> parameter.

**SIO_GET_INTERFACE_LIST_EX** is not currently supported on Windows.

</dd> <dt>

<span id="SIO_GET_QOS__opcode_setting__O__T__1_"></span><span id="sio_get_qos__opcode_setting__o__t__1_"></span><span id="SIO_GET_QOS__OPCODE_SETTING__O__T__1_"></span>**SIO_GET_QOS** (opcode setting: O, T==1)
</dt> <dd>


Retrieves the <b><a href="/en-us/previous-versions/windows/desktop/qos/qos-structures">QOS</a></b> structure associated with the socket. The input buffer is optional. Some protocols (for example, RSVP) allow the input buffer to be used to qualify a **QOS** request. The **QOS** structure will be copied into the output buffer. The output buffer must be sized large enough to be able to contain the full **QOS** structure. The WSAENOPROTOOPT error code is indicated for service providers that do not support quality of service.

</dd> <dt>

<span id="SIO_IDEAL_SEND_BACKLOG_CHANGE__opcode_setting__V__T__0_"></span><span id="sio_ideal_send_backlog_change__opcode_setting__v__t__0_"></span><span id="SIO_IDEAL_SEND_BACKLOG_CHANGE__OPCODE_SETTING__V__T__0_"></span>**SIO_IDEAL_SEND_BACKLOG_CHANGE** (opcode setting: V, T==0)
</dt> <dd>

Notifies an application when the ideal send backlog (ISB) value changes for the underlying connection.

When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput. The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size. The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).


The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system. The [**SIO_IDEAL_SEND_BACKLOG_CHANGE**](/windows/win32/winsock/sio-ideal-send-backlog-change) IOCTL can be used by an application to get notification when the ISB value changes dynamically for a connection.

For more detailed information, see the **SIO_IDEAL_SEND_BACKLOG_CHANGE** reference.

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](/windows/win32/winsock/sio-ideal-send-backlog-change) is supported on Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.

</dd> <dt>

<span id="SIO_IDEAL_SEND_BACKLOG_QUERY__opcode_setting__O__T__0_"></span><span id="sio_ideal_send_backlog_query__opcode_setting__o__t__0_"></span><span id="SIO_IDEAL_SEND_BACKLOG_QUERY__OPCODE_SETTING__O__T__0_"></span>**SIO_IDEAL_SEND_BACKLOG_QUERY** (opcode setting: O, T==0)
</dt> <dd>

Retrieves the ideal send backlog (ISB) value for the underlying connection.

When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput. The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size. The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).

The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008 and later. The **SIO_IDEAL_SEND_BACKLOG_QUERY** IOCTL can be used by an application to query the ISB value for a connection.

For more detailed information, see the [**SIO_IDEAL_SEND_BACKLOG_QUERY**](/windows/win32/winsock/sio-ideal-send-backlog-query) reference.

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](/windows/win32/winsock/sio-ideal-send-backlog-query) is supported on Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.

</dd> <dt>

<span id="SIO_KEEPALIVE_VALS__opcode_setting__I__T__3_"></span><span id="sio_keepalive_vals__opcode_setting__i__t__3_"></span><span id="SIO_KEEPALIVE_VALS__OPCODE_SETTING__I__T__3_"></span>**SIO_KEEPALIVE_VALS** (opcode setting: I, T==3)
</dt> <dd>

Enables or disables the per-connection setting of the TCP **keep-alive** option which specifies the TCP keep-alive timeout and interval. For more information on the keep-alive option, see section 4.2.3.6 on the <i>Requirements for Internet Hosts—Communication Layers</i> specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).

**SIO_KEEPALIVE_VALS** can be used to enable or disable keep-alive probes and set the keep-alive timeout and interval. The keep-alive timeout specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent. The keep-alive interval specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgment is received.

The <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> option, which is one of the SOL_SOCKET Socket Options, can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option. To query whether TCP keep-alive is enabled on a socket, the **getsockopt** function can be called with the **SO_KEEPALIVE** option. To enable or disable TCP keep-alive, the [**setsockopt**](../winsock/nf-winsock-setsockopt.md) function can be called with the <b><a href="/windows/win32/winsock/so-keepalive">SO_KEEPALIVE</a></b> option. If TCP keep-alive is enabled with **SO_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO_KEEPALIVE_VALS**.

For more detailed information, see the [**SIO_KEEPALIVE_VALS**](/windows/win32/winsock/sio-keepalive-vals) reference. **SIO_KEEPALIVE_VALS** is supported on Windows 2000 and later.

</dd> <dt>

<span id="SIO_MULTIPOINT_LOOPBACK__opcode_setting__I__T__1_"></span><span id="sio_multipoint_loopback__opcode_setting__i__t__1_"></span><span id="SIO_MULTIPOINT_LOOPBACK__OPCODE_SETTING__I__T__1_"></span>**SIO_MULTIPOINT_LOOPBACK** (opcode setting: I, T==1)
</dt> <dd>

Controls whether data sent by an application on the local computer (not necessarily by the same socket) in a multicast session will be received by a socket joined to the multicast destination group on the loopback interface. A value of **TRUE** causes multicast data sent by an application on the local computer to be delivered to a listening socket on the loopback interface. A value of **FALSE** prevents multicast data sent by an application on the local computer from being delivered to a listening socket on the loopback interface. By default, **SIO_MULTIPOINT_LOOPBACK** is enabled.

</dd> <dt>

<span id="SIO_MULTICAST_SCOPE__opcode_setting__I__T__1_"></span><span id="sio_multicast_scope__opcode_setting__i__t__1_"></span><span id="SIO_MULTICAST_SCOPE__OPCODE_SETTING__I__T__1_"></span>**SIO_MULTICAST_SCOPE** (opcode setting: I, T==1)
</dt> <dd>

Specifies the scope over which multicast transmissions will occur. Scope is defined as the number of routed network segments to be covered. A scope of zero would indicate that the multicast transmission would not be placed on the wire, but could be disseminated across sockets within the local host. A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers. Higher scope values determine the number of routers that can be crossed. Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.

</dd> <dt>

<span id="SIO_QUERY_RSS_SCALABILITY_INFO__opcode_setting__O__T__3_"></span><span id="sio_query_rss_scalability_info__opcode_setting__o__t__3_"></span><span id="SIO_QUERY_RSS_SCALABILITY_INFO__OPCODE_SETTING__O__T__3_"></span>**SIO_QUERY_RSS_SCALABILITY_INFO** (opcode setting: O, T==3)
</dt> <dd>

Queries offload interfaces for receive-side scaling (RSS) capability. The argument structure returned for **SIO_QUERY_RSS_SCALABILITY_INFO** is specified in the **RSS_SCALABILITY_INFO** structure defined in the <i>Mstcpip.h</i> header file. This structure is defined as follows.

```cpp
void CALLBACK 
CompletionRoutine(  
  IN DWORD           dwError, 
  IN DWORD           cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD           dwFlags 
);
```

The value returned in the **RssEnabled** member indicates if RSS is enabled on at least one interface.

If the output buffer is not large enough for the **RSS_SCALABILITY_INFO** structure (the <i>cbOutBuffer</i> is less than the size of a **RSS_SCALABILITY_INFO**) or the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval).

In high-speed networking where multiple CPUs reside within a single system, the ability of the networking protocol stack to scale well on a multi-CPU system is inhibited because the architecture of NDIS 5.1 and earlier versions limits receive protocol processing to a single CPU. Receive-side scaling (RSS) resolves this issue by allowing the network load from a network adapter to be balanced across multiple CPUs.

**SIO_QUERY_RSS_SCALABILITY_INFO** is supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_QUERY_WFP_ALE_ENDPOINT_HANDLE__opcode_setting__O__T__3_"></span><span id="sio_query_wfp_ale_endpoint_handle__opcode_setting__o__t__3_"></span><span id="SIO_QUERY_WFP_ALE_ENDPOINT_HANDLE__OPCODE_SETTING__O__T__3_"></span>**SIO_QUERY_WFP_ALE_ENDPOINT_HANDLE** (opcode setting: O, T==3)
</dt> <dd>

Queries the Application Layer Enforcement (ALE) endpoint handle.

The Windows Filtering Platform (WFP) supports network traffic inspection and modification. In Windows Vista, WFP focuses on scenarios where the host machine is the communication endpoint. In Windows Server 2008 , however, there are edge firewall implementations which would like to leverage the WFP platform to inspect and proxy pass-through traffic. The Internet Security and Acceleration (ISA) server is an example of such an edge device.

There are some firewall scenarios that may require the ability to inject an inbound packet into the send path associated with an existing endpoint. There needs to be a mechanism to discover the transport layer endpoint handle associated with the destination endpoint. The application that created the endpoint owns these transport layer endpoints. This IOCTL is used to provide socket handle to transport layer endpoint handle mapping.

If the output buffer is not large enough for the endpoint handle (the <i>cbOutBuffer</i> is less than the size of a **UINT64**) or the <i>lpvOutBuffer</i> parameter is a **NULL** pointer, **SOCKET_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval).

**SIO_QUERY_WFP_ALE_ENDPOINT_HANDLE** is supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_QUERY_PNP_TARGET_HANDLE__opcode_setting__O__T__1_"></span><span id="sio_query_pnp_target_handle__opcode_setting__o__t__1_"></span><span id="SIO_QUERY_PNP_TARGET_HANDLE__OPCODE_SETTING__O__T__1_"></span>**SIO_QUERY_PNP_TARGET_HANDLE** (opcode setting: O, T==1)
</dt> <dd>

To obtain the socket descriptor of the next provider in the chain on which the current socket depends in PnP sense. This IOCTL is invoked by the Windows Sockets 2 DLL only on sockets of non-IFS service providers created through [**WPUCreateSocketHandle**](./nf-ws2spi-wpucreatesockethandle.md) call. The provider should return in the output buffer the socket handle of the next provider in the chain on which a given socket handle depends in PnP sense (for example, the removal of the device that supports the underlying handle will result in the invalidation of the handle above it in the chain).

If an overlapped operation completes immediately, this function returns a value of zero and the <i>lpcbBytesReturned</i> parameter is updated with the number of bytes in the output buffer. If the overlapped operation is successfully initiated and will complete later, this function returns SOCKET_ERROR and indicates error code WSA_IO_PENDING. In this case, <i>lpcbBytesReturned</i> is not updated. When the overlapped operation completes, the amount of data in the output buffer is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>.

</dd> <dt>

<span id="SIO_RCVALL__opcode_setting__I__T__3_"></span><span id="sio_rcvall__opcode_setting__i__t__3_"></span><span id="SIO_RCVALL__OPCODE_SETTING__I__T__3_"></span>**SIO_RCVALL** (opcode setting: I, T==3)
</dt> <dd>


Enables a socket to receive all IPv4 or IPv6 packets passing through a network interface. The socket handle passed to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function must be one of the following:

-   An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.
-   An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.

The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR_ANY** or **in6addr_any**.

On Windows Server 2008 and earlier, the [**SIO_RCVALL**](/windows/win32/winsock/sio-rcvall) IOCTL setting would not capture local packets sent out of a network interface. This included packets received on another interface and forwarded out the network interface specified for the **SIO_RCVALL** IOCTL.

On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured. This includes packets received on another interface and then forwarded out the network interface bound to the socket with [**SIO_RCVALL**](/windows/win32/winsock/sio-rcvall) IOCTL.

Setting this IOCTL requires Administrator privilege on the local computer.

This feature is sometimes referred to as promiscuous mode.

The possible values for the **SIO_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the <i>Mstcpip.h</i> header file. The possible values for SIO_RCVALL are as follows:



| Term                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL_OFF<br/>                                     | Disable this option so a socket does not receive all IPv4 or IPv6 packets on the network. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL_ON<br/>                                        | Enable this option so a socket receives all IPv4 or IPv6 packets on the network. This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode. On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment. All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket. <br/> This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.<br/> Netmon uses the same mode for the network interface, but does not use this option to capture traffic.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL_SOCKETLEVELONLY<br/> | This feature is not currently implemented, so setting this option does not have any affect.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL_IPLEVEL<br/>                         | Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level on the network. This option does not enable promiscuous mode on the network interface card. This option only affects packet processing at the IP level. The NIC still receives only packets directed to its configured unicast and multicast addresses. However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.<br/> This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.<br/>                                                                                             |


For more detailed information, see the [**SIO_RCVALL**](/windows/win32/winsock/sio-rcvall) reference.

**SIO_RCVALL** is supported on Windows 2000 and later.

</dd> <dt>

<span id="SIO_RELEASE_PORT_RESERVATION__opcode_setting__I__T__3_"></span><span id="sio_release_port_reservation__opcode_setting__i__t__3_"></span><span id="SIO_RELEASE_PORT_RESERVATION__OPCODE_SETTING__I__T__3_"></span>**SIO_RELEASE_PORT_RESERVATION** (opcode setting: I, T==3)
</dt> <dd>


Releases a runtime reservation for a block of TCP or UDP ports. The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](/windows/win32/winsock/sio-acquire-port-reservation) IOCTL.

For more detailed information, see the [**SIO_RELEASE_PORT_RESERVATION**](/windows/win32/winsock/sio-release-port-reservation) reference.

[**SIO_RELEASE_PORT_RESERVATION**](/windows/win32/winsock/sio-release-port-reservation) is supported on Windows Vista and later versions of the operating system.

</dd> <dt>

<span id="SIO_ROUTING_INTERFACE_CHANGE__opcode_setting__I__T__1_"></span><span id="sio_routing_interface_change__opcode_setting__i__t__1_"></span><span id="SIO_ROUTING_INTERFACE_CHANGE__OPCODE_SETTING__I__T__1_"></span>**SIO_ROUTING_INTERFACE_CHANGE** (opcode setting: I, T==1)
</dt> <dd>

To receive notification of a routing interface change that should be used to reach the remote address in the input buffer (specified as a <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> structure). No output information on the new routing interface will be provided upon completion of this IOCTL; the completion merely indicates that the routing interface for a given destination has changed and should be queried using the **SIO_ROUTING_INTERFACE_QUERY** IOCTL.

It is assumed (although not required) that the application uses overlapped I/O to be notified of the routing interface change through completion of **SIO_ROUTING_INTERFACE_CHANGE** request. Alternatively, if the **SIO_ROUTING_INTERFACE_CHANGE** IOCTL is issued on a non-blocking socket with the <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters set to **NULL**), it will complete immediately with error [WSAEWOULDBLOCK](/windows/win32/winsock/windows-sockets-error-codes-2#wsaewouldblock) and the Windows Socket SPI client can then wait for routing change events using a call to [**LPWSPEventSelect**](./nc-ws2spi-lpwspeventselect.md) or **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** with the FD_ROUTING_INTERFACE_CHANGE bit set in the network event bitmask.

It is recognized that routing information remains stable in most cases so that requiring the application to keep multiple outstanding IOCTLs to get notifications about all destinations that it is interested in as well as having the service provider keep track of these notification requests will use a significant amount system resources. This situation can be avoided by extending the meaning of the input parameters and relaxing the service provider requirements as follows:

The Windows Sockets SPI client can specify a protocol family specific wildcard address (same as one used in <b><a href="/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b> call when requesting to bind to any available address) to request notifications of any routing changes. This allows the Windows Sockets SPI client to keep only one outstanding **SIO_ROUTING_INTERFACE_CHANGE** for all the sockets and destinations it has and then use **SIO_ROUTING_INTERFACE_QUERY** to get the actual routing information.

The service provider can opt to ignore the information supplied by the Windows Sockets SPI client in the input buffer of the **SIO_ROUTING_INTERFACE_CHANGE** (as though the Windows Sockets SPI client specified a wildcard address) and complete the **SIO_ROUTING_INTERFACE_CHANGE** IOCTL or signal FD_ROUTING_INTERFACE_CHANGE event in the event of any routing information change (not just the route to the destination specified in the input buffer).

</dd> <dt>

<span id="SIO_ROUTING_INTERFACE_QUERY__opcode_setting__I__O__T__1_"></span><span id="sio_routing_interface_query__opcode_setting__i__o__t__1_"></span><span id="SIO_ROUTING_INTERFACE_QUERY__OPCODE_SETTING__I__O__T__1_"></span>**SIO_ROUTING_INTERFACE_QUERY** (opcode setting: I, O, T==1)
</dt> <dd>

To obtain the address of the local interface (represented as <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> structure) that should be used to send to the remote address specified in the input buffer (as **sockaddr**). Remote multicast addresses may be submitted in the input buffer to get the address of the preferred interface for multicast transmission. In any case, the interface address returned may be used by the application in a subsequent <b><a href="/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b> request.

Note that routes are subject to change. Therefore, Windows Socket SPI clients cannot rely on the information returned by **SIO_ROUTING_INTERFACE_QUERY** to be persistent. SPI clients may register for routing change notifications using the **SIO_ROUTING_INTERFACE_CHANGE** IOCTL, which provides for notification through either overlapped I/O or a FD_ROUTING_INTERFACE_CHANGE event. The following sequence of actions can be used to guarantee that the Windows Socket SPI client always has current routing interface information for a given destination:

-   Issue **SIO_ROUTING_INTERFACE_CHANGE** IOCTL.
-   Issue **SIO_ROUTING_INTERFACE_QUERY** IOCTL.
-   Whenever **SIO_ROUTING_INTERFACE_CHANGE** IOCTL notifies the WinSock SPI client of routing change (either through overlapped I/O or by signaling FD_ROUTING_INTERFACE_CHANGE event), the whole sequence of actions should be repeated.


If output buffer is not large enough to contain the interface address, SOCKET_ERROR is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAEFAULT](/windows/win32/winsock/windows-sockets-error-codes-2#wsaefault). The required size of the output buffer will be returned in <i>lpcbBytesReturned</i> in this case. Note the WSAEFAULT error code is also returned if the <i>lpvInBuffer</i>, <i>lpvOutBuffer</i>, or <i>lpcbBytesReturned</i> parameter is not totally contained in a valid part of the user address space.

If the destination address specified in the input buffer cannot be reached through any of the available interfaces, SOCKET_ERROR is returned as the result of this IOCTL and [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) returns [WSAENETUNREACH](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenetunreach) or even [WSAENETDOWN](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenetdown) if all of the network connectivity is lost.

</dd> <dt>

<span id="SIO_SET_COMPATIBILITY_MODE__opcode_setting__I__T__3_"></span><span id="sio_set_compatibility_mode__opcode_setting__i__t__3_"></span><span id="SIO_SET_COMPATIBILITY_MODE__OPCODE_SETTING__I__T__3_"></span>**SIO_SET_COMPATIBILITY_MODE** (opcode setting: I, T==3)
</dt> <dd>

Requests how the networking stack should handle certain behaviors for which the default way of handling the behavior may differ across Windows versions. The argument structure for **SIO_SET_COMPATIBILITY_MODE** is specified in the **WSA_COMPATIBILITY_MODE** structure defined in the <i>Mswsockdef.h</i> header file. This structure is defined as follows:


```C++
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```



The value specified in the **BehaviorId** member indicates the behavior requested. The value specified in the **TargetOsVersion** member indicates the Windows version that is being requested for the behavior.

The **BehaviorId** member can be one of the values from the **WSA_COMPATIBILITY_BEHAVIOR_ID** enumeration type defined in the <i>Mswsockdef.h</i> header file. The possible values for the **BehaviorId** member are as follows



| Term                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | This is equivalent to requesting all of the possible compatible behaviors defined for **WSA_COMPATIBILITY_BEHAVIOR_ID**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | When the **TargetOsVersion** member is set to a value for Windows Vista or later, reductions to the TCP receive buffer size on this socket using the **SO_RCVBUF** socket option are allowed even after a TCP connection has been establishment. <br/> When the **TargetOsVersion** member is set to a value earlier than Windows Vista, reductions to the TCP receive buffer size on this socket using the **SO_RCVBUF** socket option are not allowed after connection establishment. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | When the **TargetOsVersion** member is set to a value for Windows Vista or later, receive window auto-tuning is enabled and the TCP window scale factor is reduced to 2 from the default value of 8.<br/> When the **TargetOsVersion** is set to a value earlier than Windows Vista, receive window auto-tuning is disabled. The TCP window scaling option is also disabled and the maximum true receive window size is limited to 65,535 bytes. The TCP window scaling option can't be negotiated on the connection even if the **SO_RCVBUF** socket option was called on this socket specifying a value greater than 65,535 bytes before the connection was established.<br/> |



 

For more detailed information, see the **SIO_SET_COMPATIBILITY_MODE** reference.

**SIO_SET_COMPATIBILITY_MODE** is supported on Windows Vista and later.

</dd> <dt>

<span id="SIO_SET_GROUP_QOS__opcode_setting__I__T__1_"></span><span id="sio_set_group_qos__opcode_setting__i__t__1_"></span><span id="SIO_SET_GROUP_QOS__OPCODE_SETTING__I__T__1_"></span>**SIO_SET_GROUP_QOS** (opcode setting: I, T==1)
</dt> <dd>

Reserved.

</dd> <dt>

<span id="SIO_SET_QOS__opcode_setting__I__T__1_"></span><span id="sio_set_qos__opcode_setting__i__t__1_"></span><span id="SIO_SET_QOS__OPCODE_SETTING__I__T__1_"></span>**SIO_SET_QOS** (opcode setting: I, T==1)
</dt> <dd>

Associate the supplied <b><a href="/en-us/previous-versions/windows/desktop/qos/qos-structures">QOS</a></b> structure with the socket. No output buffer is required, the **QOS** structure will be obtained from the input buffer. The WSAENOPROTOOPT error code is indicated for service providers that do not support quality of service.

</dd> <dt>

<span id="SIO_TRANSLATE_HANDLE__opcode_setting__I__O__T__1_"></span><span id="sio_translate_handle__opcode_setting__i__o__t__1_"></span><span id="SIO_TRANSLATE_HANDLE__OPCODE_SETTING__I__O__T__1_"></span>**SIO_TRANSLATE_HANDLE** (opcode setting: I, O, T==1)
</dt> <dd>

To obtain a corresponding handle for socket <i>s</i> that is valid in the context of a companion interface (for example, TH_NETDEV and TH_TAPI). A manifest constant identifying the companion interface along with any other needed parameters are specified in the input buffer. The corresponding handle will be available in the output buffer upon completion of this function. Refer to the appropriate section in the <i>Windows Sockets 2 Protocol-Specific Annex</i> and/or documentation for the particular companion interface for additional details. The <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a>  error code is indicated for service providers that do not support this IOCTL for the specified companion interface. This IOCTL retrieves the handle associated using **SIO_TRANSLATE_HANDLE**.

It is recommended that COM be used instead of this IOCTL to discover and track other interfaces that might be supported by a socket. This IOCTL is present for backward compatibility with systems where COM is not available or cannot be used for some other reason.

</dd> <dt>

<span id="SIO_UDP_CONNRESET__opcode_setting__I__T__3_"></span><span id="sio_udp_connreset__opcode_setting__i__t__3_"></span><span id="SIO_UDP_CONNRESET__OPCODE_SETTING__I__T__3_"></span>**SIO_UDP_CONNRESET** (opcode setting: I, T==3)
</dt> <dd>

**Windows XP:** Controls whether UDP PORT_UNREACHABLE messages are reported. Set to **TRUE** to enable reporting. Set to **FALSE** to disable reporting.

</dd> </dl>

When called with an overlapped socket, the <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation.

If the <i>lpCompletionRoutine</i> parameter is **NULL**, the service provider signals the **hEvent** member of <i>lpOverlapped</i> when the overlapped operation completes if it contains a valid event object handle. The Windows Sockets SPI client can use <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a> to poll or wait on the event object.

If <i>lpCompletionRoutine</i> is not **NULL**, the **hEvent** member is ignored and can be used by the Windows Sockets SPI client to pass context information to the completion routine. A client that passes a non-**NULL** <i>lpCompletionRoutine</i> and later calls <b><a href="/windows/win32/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a></b> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of **WSAGetOverlappedResult** to **TRUE**. In this case, the usage of the **hEvent** member is undefined, and attempting to wait on the **hEvent** member would produce unpredictable results.

It is the service provider's responsibility to arrange for invocation of the client specified–completion routine when the overlapped operation completes. Since the completion routine must be executed in the context of the same thread that initiated the overlapped operation, it cannot be invoked directly from the service provider. The WS2_32.DLL offers an asynchronous procedure call (APC) mechanism to facilitate invocation of completion routines.

A service provider arranges for a function to be executed in the proper thread and process context by calling <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. This function can be called from any process and thread context, even a context different from the thread and process that was used to initiate the overlapped operation.

<b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b> takes as input parameters a pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure (supplied to the provider through the <i>lpThreadId</i> input parameter), a pointer to an APC function to be invoked, and a 32-bit context value that is subsequently passed to the APC function. Because only a single 32-bit context value is available, the APC function itself cannot be the client specified–completion routine. The service provider must instead supply a pointer to its own APC function that uses the supplied context value to access the needed result information for the overlapped operation, and then invokes the client specified–completion routine.

The prototype for the client-supplied completion routine is as follows:


```C++
);
```



**CompletionRoutine** is a placeholder for a client supplied function. The <i>dwError</i> specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> specifies the number of bytes returned. Currently, there are no flag values defined and <i>dwFlags</i> will be zero. This function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. The completion routines can be called in any order, though not necessarily in the same order that the overlapped operations are completed.

### Compatibility

The IOCTL codes with T == 0 are a subset of the IOCTL codes used in Berkeley sockets. In particular, there is no command that is equivalent to FIOASYNC.

> [!Note]  
> All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the operations complete. See <b><a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a></b> for more information.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>
   
<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>