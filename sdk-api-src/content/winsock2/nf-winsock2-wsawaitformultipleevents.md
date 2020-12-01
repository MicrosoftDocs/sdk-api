---
UID: NF:winsock2.WSAWaitForMultipleEvents
title: WSAWaitForMultipleEvents function (winsock2.h)
description: Returns when one or all of the specified event objects are in the signaled state, when the time-out interval expires, or when an I/O completion routine has executed.
helpviewer_keywords: ["WSAWaitForMultipleEvents","WSAWaitForMultipleEvents function [Winsock]","_win32_wsawaitformultipleevents_2","winsock.wsawaitformultipleevents_2","winsock2/WSAWaitForMultipleEvents"]
old-location: winsock\wsawaitformultipleevents_2.htm
tech.root: WinSock
ms.assetid: 7a978ade-6323-455b-b655-f372f4bcadc8
ms.date: 12/05/2018
ms.keywords: WSAWaitForMultipleEvents, WSAWaitForMultipleEvents function [Winsock], _win32_wsawaitformultipleevents_2, winsock.wsawaitformultipleevents_2, winsock2/WSAWaitForMultipleEvents
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAWaitForMultipleEvents
 - winsock2/WSAWaitForMultipleEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAWaitForMultipleEvents
---

# WSAWaitForMultipleEvents function


## -description

The 
<b>WSAWaitForMultipleEvents</b> function returns when one or all of the specified event objects are in the signaled state, when the time-out interval expires, or when an I/O completion routine has executed.

## -parameters

### -param cEvents [in]

The number of event object handles in the array pointed to by <i>lphEvents</i>. The maximum number of event object handles is <b>WSA_MAXIMUM_WAIT_EVENTS</b>. One or more events must be specified.

### -param lphEvents [in]

A pointer to an array of event object handles. The array can contain handles of objects of different types. It may not contain multiple copies of the same handle if the <i>fWaitAll</i> parameter is set to <b>TRUE</b>. 
If one of these handles is closed while the wait is still pending, the behavior of <b>WSAWaitForMultipleEvents</b> is undefined.

The handles must have the <b>SYNCHRONIZE</b> access right.  For more information, see <a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>.

### -param fWaitAll [in]

A value that specifies the wait type. If <b>TRUE</b>, the function returns when the state of all objects in the <i>lphEvents</i> array is signaled. If <b>FALSE</b>, the function returns when any  of the event objects is signaled. In the latter case, the return value minus <b>WSA_WAIT_EVENT_0</b> indicates the index of the event object whose state caused the function to return. If more than one event object became signaled during the call, this is the array index to the signaled event object with the smallest index value of all the signaled event objects.

### -param dwTimeout [in]

The time-out interval, in milliseconds. <b>WSAWaitForMultipleEvents</b> returns if the time-out interval expires, even if conditions specified by the <i>fWaitAll</i> parameter are not satisfied. If the <i>dwTimeout</i> parameter is zero, <b>WSAWaitForMultipleEvents</b> tests the state of the specified event objects and returns immediately. If <i>dwTimeout</i> is <b>WSA_INFINITE</b>, <b>WSAWaitForMultipleEvents</b> waits forever; that is, the time-out interval never expires.

### -param fAlertable [in]

A value that specifies whether the thread is placed in an alertable wait state so the system can execute I/O completion routines. If <b>TRUE</b>, the thread is placed in an alertable wait state and <b>WSAWaitForMultipleEvents</b> can return when the system executes an I/O completion routine. In this case, <b>WSA_WAIT_IO_COMPLETION</b> is returned and the event that was being waited on is not signaled yet. The application must call the <b>WSAWaitForMultipleEvents</b> function again. If <b>FALSE</b>, the thread is not placed in an alertable wait state and I/O completion routines are not executed.

## -returns

If the 
<b>WSAWaitForMultipleEvents</b> function succeeds,  the return value upon success is one of the following values.

<table>
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSA_WAIT_EVENT_0 to (WSA_WAIT_EVENT_0 + cEvents - 1)</b></dt>
</dl>
</td>
<td width="60%">
If the <i>fWaitAll</i> parameter is <b>TRUE</b>, the return value indicates that all specified event objects is signaled. 

If the <i>fWaitAll</i> parameter is <b>FALSE</b>, the return value minus <b>WSA_WAIT_EVENT_0</b> indicates the <i>lphEvents</i> array index of the signaled event object that satisfied the wait. If more than one event object became signaled during the call, the return value indicates the <i>lphEvents</i> array index of the signaled event object with the smallest index value of all the signaled event objects. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSA_WAIT_IO_COMPLETION</b></dt>
</dl>
</td>
<td width="60%">
The wait was ended by one or more I/O completion routines that were executed. The event that was being waited on is not signaled yet. The application must call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> function again. This return value can only be returned if the <i>fAlertable</i> parameter is <b>TRUE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSA_WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out interval elapsed and the conditions specified by the <i>fWaitAll</i> parameter were not satisfied. No I/O completion routines were executed.

</td>
</tr>
</table>
 

If the <b>WSAWaitForMultipleEvents</b> function fails, the return value is <b>WSA_WAIT_FAILED</b>. The following table lists values that can be used with <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> to get extended error information. 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>Not enough free memory was available to complete the operation.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></td>
<td>One or more of the values in the <i>lphEvents</i> array is not a valid event object handle.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_PARAMETER</a></td>
<td>The <i>cEvents</i> parameter does not contain a valid handle count.</td>
</tr>
</table>

## -remarks

The <b>WSAWaitForMultipleEvents</b> function determines whether the wait criteria have been met. If the criteria have not been met, the calling thread enters the wait state. It uses no processor time while waiting for the criteria to be met.

The 
<b>WSAWaitForMultipleEvents</b> function returns when any one or all of the specified objects are in the signaled state, or when the time-out interval elapses.

When the <i>bWaitAll</i> parameter is <b>TRUE</b>, the wait operation is completed only when the states of all objects have been set to signaled. The function does not modify the states of the specified objects until the states of all objects have been set to signaled. 

When <i>bWaitAll</i> parameter is <b>FALSE</b>, <b>WSAWaitForMultipleEvents</b> checks the handles in the <i>lphEvents</i> array in order starting with index 0, until one of the objects is signaled. If multiple objects become signaled, the function returns the index of the first handle in the <i>lphEvents</i> array whose object was signaled.

This function is also used to perform an alertable wait by setting the <i>fAlertable</i> parameter to <b>TRUE</b>. This enables the function to return when the system executes an I/O completion routine by the calling thread.

A thread must be in an alertable wait state in order for the system to execute I/O completion routines (asynchronous procedure calls or APCs). So if an application calls <b>WSAWaitForMultipleEvents</b> when there are pending asynchronous operations that have I/O completion routines and the <i>fAlertable</i> parameter is <b>FALSE</b>, then those I/O completion routines will not be executed even if those I/O operations are completed.

If the <i>fAlertable</i> parameter is <b>TRUE</b> and one of the pending operations completes, the APC is executed and <b>WSAWaitForMultipleEvents</b> will return <b>WSA_IO_COMPLETION</b>.
The pending event is not signaled yet. The application must call the <b>WSAWaitForMultipleEvents</b> function again.

Applications that require an alertable wait state without waiting for any event objects to be signaled should use the Windows 
<a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a> function.

The current implementation of <b>WSAWaitForMultipleEvents</b> calls the <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function.

<div class="alert"><b>Note</b>  Use caution when calling the <b>WSAWaitForMultipleEvents</b> with code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses <b>WSAWaitForMultipleEvents</b> with no time-out limit (the <i>dwTimeout</i> parameter set to <b>WSA_INFINITE</b>) may cause the system to become deadlocked.</div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code example shows how to use the <b>WSAWaitForMultipleEvents</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

#define DATA_BUFSIZE 4096

int main()
{
    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData = { 0 };
    int iResult = 0;
    BOOL bResult = TRUE;

    WSABUF DataBuf;
    char buffer[DATA_BUFSIZE];

    DWORD EventTotal = 0;
    DWORD RecvBytes = 0;
    DWORD Flags = 0;
    DWORD BytesTransferred = 0;

    WSAEVENT EventArray[WSA_MAXIMUM_WAIT_EVENTS];
    WSAOVERLAPPED AcceptOverlapped;
    SOCKET ListenSocket = INVALID_SOCKET;
    SOCKET AcceptSocket = INVALID_SOCKET;

    DWORD Index;

    //-----------------------------------------
    // Initialize Winsock
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
    //-----------------------------------------
    // Create a listening socket bound to a local
    // IP address and the port specified
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    u_short port = 27015;
    char *ip;
    sockaddr_in service;
    service.sin_family = AF_INET;
    service.sin_port = htons(port);
    hostent *thisHost;

    thisHost = gethostbyname("");
    if (thisHost == NULL) {
        wprintf(L"gethostbyname failed with error = %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    ip = inet_ntoa(*(struct in_addr *) *thisHost->h_addr_list);

    service.sin_addr.s_addr = inet_addr(ip);

    //-----------------------------------------
    // Bind the listening socket to the local IP address
    // and port number
    iResult = bind(ListenSocket, (SOCKADDR *) & service, sizeof (SOCKADDR));
    if (iResult != 0) {
        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    //-----------------------------------------
    // Set the socket to listen for incoming
    // connection requests
    iResult = listen(ListenSocket, 1);
    if (iResult != 0) {
        wprintf(L"listen failed with error = %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    wprintf(L"Listening...\n");

    //-----------------------------------------
    // Accept and incoming connection request
    AcceptSocket = accept(ListenSocket, NULL, NULL);
    if (AcceptSocket == INVALID_SOCKET) {
        wprintf(L"accept failed with error = %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    wprintf(L"Client Accepted...\n");

    //-----------------------------------------
    // Create an event handle and setup an overlapped structure.
    EventArray[EventTotal] = WSACreateEvent();
    if (EventArray[EventTotal] == WSA_INVALID_EVENT) {
        wprintf(L"WSACreateEvent failed with error = %d\n", WSAGetLastError());
        closesocket(AcceptSocket);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }

    ZeroMemory(&AcceptOverlapped, sizeof (WSAOVERLAPPED));
    AcceptOverlapped.hEvent = EventArray[EventTotal];

    DataBuf.len = DATA_BUFSIZE;
    DataBuf.buf = buffer;

    EventTotal++;

    //-----------------------------------------
    // Call WSARecv to receive data into DataBuf on 
    // the accepted socket in overlapped I/O mode
    if (WSARecv(AcceptSocket, &DataBuf, 1, &RecvBytes, &Flags, &AcceptOverlapped, NULL) ==
        SOCKET_ERROR) {
        iResult = WSAGetLastError();
        if (iResult != WSA_IO_PENDING)
            wprintf(L"WSARecv failed with error = %d\n", iResult);
    }
    //-----------------------------------------
    // Process overlapped receives on the socket
    while (1) {

        //-----------------------------------------
        // Wait for the overlapped I/O call to complete
        Index = WSAWaitForMultipleEvents(EventTotal, EventArray, FALSE, WSA_INFINITE, FALSE);

        //-----------------------------------------
        // Reset the signaled event
        bResult = WSAResetEvent(EventArray[Index - WSA_WAIT_EVENT_0]);
        if (bResult == FALSE) {
            wprintf(L"WSAResetEvent failed with error = %d\n", WSAGetLastError());
        }
        //-----------------------------------------
        // Determine the status of the overlapped event
        bResult =
            WSAGetOverlappedResult(AcceptSocket, &AcceptOverlapped, &BytesTransferred, FALSE,
                                   &Flags);
        if (bResult == FALSE) {
            wprintf(L"WSAGetOverlappedResult failed with error = %d\n", WSAGetLastError());
        }
        //-----------------------------------------
        // If the connection has been closed, close the accepted socket
        if (BytesTransferred == 0) {
            wprintf(L"Closing accept Socket %d\n", AcceptSocket);
            closesocket(ListenSocket);
            closesocket(AcceptSocket);
            WSACloseEvent(EventArray[Index - WSA_WAIT_EVENT_0]);
            WSACleanup();
            return 1;
        }
        //-----------------------------------------
        // If data has been received, echo the received data
        // from DataBuf back to the client
        iResult =
            WSASend(AcceptSocket, &DataBuf, 1, &RecvBytes, Flags, &AcceptOverlapped, NULL);
        if (iResult != 0) {
            wprintf(L"WSASend failed with error = %d\n", WSAGetLastError());
        }
        //-----------------------------------------         
        // Reset the changed flags and overlapped structure
        Flags = 0;
        ZeroMemory(&AcceptOverlapped, sizeof (WSAOVERLAPPED));

        AcceptOverlapped.hEvent = EventArray[Index - WSA_WAIT_EVENT_0];

        //-----------------------------------------
        // Reset the data buffer
        DataBuf.len = DATA_BUFSIZE;
        DataBuf.buf = buffer;
    }

    closesocket(ListenSocket);
    closesocket(AcceptSocket);
    WSACleanup();

    return 0;
}


```


<b>Windows Phone 8:</b> This  function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>