---
UID: NF:iphlpapi.NotifyRouteChange
title: NotifyRouteChange function (iphlpapi.h)
author: windows-sdk-content
description: The NotifyRouteChange function causes a notification to be sent to the caller whenever a change occurs in the IPv4 routing table.
old-location: iphlp\notifyroutechange.htm
tech.root: IpHlp
ms.assetid: 39f2ec4d-131a-4a0a-9740-0d96aaea2dc7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NotifyRouteChange, NotifyRouteChange function [IP Helper], _iphlp_notifyroutechange, iphlp.notifyroutechange, iphlpapi/NotifyRouteChange
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - NotifyRouteChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NotifyRouteChange function


## -description


The 
<b>NotifyRouteChange</b> function causes a notification to be sent to the caller whenever a change occurs in the IPv4 routing table.


## -parameters




### -param Handle [out]

A pointer to a <b>HANDLE</b> variable that receives a handle to use in asynchronous notification.


### -param overlapped [in]

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that  notifies the caller of any changes in the routing table.


## -returns



If the function succeeds, the return value is NO_ERROR if the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters. If the caller specifies non-<b>NULL</b> parameters, the return value for success is ERROR_IO_PENDING. If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

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
<b>NotifyRouteChange</b> function may be called in two ways:<ul>
<li>Synchronous method</li>
<li>Asynchronous method</li>
</ul>


If the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters, the call to 
<b>NotifyRouteChange</b> is synchronous and will block until  an IPv4 routing table change occurs. In this case if a change occurs, the <b>NotifyRouteChange</b> function completes to indicate that a change has occurred. 

If the <b>NotifyRouteChange</b> function is called synchronously, a notification will be sent on the next IPv4 routing change until the application terminates. 

If the caller specifies a handle variable and an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, the caller can use the returned handle with the <b>OVERLAPPED</b> structure to receive asynchronous notification of IPv4 routing table changes. See the following topics for information about using the handle and 
<b>OVERLAPPED</b> structure to receive notifications:

<ul>
<li>
<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O Completion Ports</a>
</li>
</ul>
If the application receives a notification and requires notification for the next change, then the <b>NotifyRouteChange</b> function must be called again.

The <a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a> function cancels notification of IP address and route changes previously requested with successful calls to the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> or <b>NotifyRouteChange</b> functions.

Once an application has been notified of a change, the application can then call the <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> or <a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a> function to retrieve the IPv4 routing table to determine what has changed. If the application is notified and requires notification for the next change, then the <b>NotifyRouteChange</b> function must be called again.

If the <b>NotifyRouteChange</b> function is called asynchronously, a notification will be sent on the next IPv4 route change until either the application cancels the notification by calling the <a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a> function or the application terminates. If the application terminates, the system will automatically cancel the registration for the notification. It is still recommended that an application explicitly cancel any notification before it terminates.  

Any registration for a notification does not persist across a system shut down or reboot.

On Windows Vista and later, the 
<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a> function  can be used to  register to be notified for changes to the IPv6 routing table  on the local computer.


#### Examples

The following example waits for a change to occur in the IP routing table.


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

  ret = NotifyRouteChange(&hand, &overlap);

  if (ret != NO_ERROR)
  {
    if (WSAGetLastError() != WSA_IO_PENDING)
    {
      printf("NotifyRouteChange error...%d\n", WSAGetLastError());            
      return;
    }
  }

  if ( WaitForSingleObject(overlap.hEvent, INFINITE) == WAIT_OBJECT_0 )
    printf("Routing table changed..\n");
}

```





## -see-also




<a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a>



<a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

