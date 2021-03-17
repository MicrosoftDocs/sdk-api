---
UID: NF:iphlpapi.NotifyAddrChange
title: NotifyAddrChange function (iphlpapi.h)
description: The NotifyAddrChange function causes a notification to be sent to the caller whenever a change occurs in the table that maps IPv4 addresses to interfaces.
helpviewer_keywords: ["NotifyAddrChange","NotifyAddrChange function [IP Helper]","_iphlp_notifyaddrchange","iphlp.notifyaddrchange","iphlpapi/NotifyAddrChange"]
old-location: iphlp\notifyaddrchange.htm
tech.root: IpHlp
ms.assetid: 22ac3b5b-452c-454b-8fbd-47a873675c6c
ms.date: 12/05/2018
ms.keywords: NotifyAddrChange, NotifyAddrChange function [IP Helper], _iphlp_notifyaddrchange, iphlp.notifyaddrchange, iphlpapi/NotifyAddrChange
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NotifyAddrChange
 - iphlpapi/NotifyAddrChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - NotifyAddrChange
---

# NotifyAddrChange function


## -description

The 
<b>NotifyAddrChange</b> function causes a notification to be sent to the caller whenever a change occurs in the table that maps IPv4 addresses to interfaces.

## -parameters

### -param Handle [out]

A pointer to a <b>HANDLE</b> variable that receives a file handle for use in a subsequent call to the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function. 

<div class="alert"><b>Warning</b>  Do not close this handle, and do not associate it with a completion port.</div>
<div> </div>

### -param overlapped [in]

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that  notifies the caller of any changes in the table that maps IP addresses to interfaces.

## -returns

If the function succeeds, the return value is NO_ERROR if the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters. If the caller specifies non-<b>NULL</b> parameters, the return value for success is ERROR_IO_PENDING.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The context is being deregistered, so the call was canceled immediately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the both the <i>Handle</i> and <i>overlapped</i> parameters are not <b>NULL</b>, but the memory specified by the
    input parameters cannot be written by the calling process.  This error is also returned if the client already has made a change notification request, so this duplicate request will fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This error is returned on versions of Windows where this function is not supported such as Windows 98/95 and Windows NT 4.0.

</td>
</tr>
</table>

## -remarks

The  
<b>NotifyAddrChange</b> function may be called in two ways:<ul>
<li>Synchronous method</li>
<li>Asynchronous method</li>
</ul>


If the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters, the call to 
<b>NotifyAddrChange</b> is synchronous and will block until an IP address change occurs. In this case if a change occurs, the <b>NotifyAddrChange</b> function completes to indicate that a change has occurred. 

If the <b>NotifyAddrChange</b> function is called synchronously, a notification will be sent on the next IPv4 address change until the application terminates. 

If the caller specifies a handle variable and an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, then the <b>NotifyAddrChange</b> function call is asynchronous and the caller can use the returned handle with the <b>OVERLAPPED</b> structure to receive asynchronous notification of IPv4 address changes using the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function. See the following topics for information about using the handle and 
<b>OVERLAPPED</b> structure to receive notifications:

<ul>
<li>
<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>
</li>
<li>
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>
</li>
</ul>
The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-cancelipchangenotify">CancelIPChangeNotify</a> function cancels notification of IPv4 address and route changes previously requested with successful calls to the <b>NotifyAddrChange</b> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a> functions.

Once an application has been notified of a change, the application can then call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function to retrieve the table of IPv4 addresses to determine what has changed. If the application is notified and requires notification for the next change, then the <b>NotifyAddrChange</b> function must be called again.

If the <b>NotifyAddrChange</b> function is called asynchronously, a notification will be sent on the next IPv4 address change until either the application cancels the notification by calling the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-cancelipchangenotify">CancelIPChangeNotify</a> function or the application terminates. If the application terminates, the system will automatically cancel the registration for the notification. It is still recommended that an application explicitly cancel any notification before it terminates.  

Any registration for a notification does not persist across a system shut down or reboot.

On Windows Vista and later, the 
<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a> function  can be used to  register to be notified for changes to IPv4 and IPv6 interfaces on  the local computer.


#### Examples

The following example waits for a change to occur in the table that maps IP addresses to interfaces.


```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <windows.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

void main()
{
  OVERLAPPED overlap;
  DWORD ret;
    
  HANDLE hand = NULL;
  overlap.hEvent = WSACreateEvent();

  ret = NotifyAddrChange(&hand, &overlap);

  if (ret != NO_ERROR)
  {
    if (WSAGetLastError() != WSA_IO_PENDING)
    {
      printf("NotifyAddrChange error...%d\n", WSAGetLastError());            
      return;
    }
  }

  if ( WaitForSingleObject(overlap.hEvent, INFINITE) == WAIT_OBJECT_0 )
    printf("IP Address table changed..\n");
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-cancelipchangenotify">CancelIPChangeNotify</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>