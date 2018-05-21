---
UID: NF:iphlpapi.NotifyAddrChange
title: NotifyAddrChange function
author: windows-driver-content
description: The NotifyAddrChange function causes a notification to be sent to the caller whenever a change occurs in the table that maps IPv4 addresses to interfaces.
old-location: iphlp\notifyaddrchange.htm
old-project: IpHlp
ms.assetid: 22ac3b5b-452c-454b-8fbd-47a873675c6c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: NotifyAddrChange, NotifyAddrChange function [IP Helper], _iphlp_notifyaddrchange, iphlp.notifyaddrchange, iphlpapi/NotifyAddrChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	NotifyAddrChange
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# NotifyAddrChange function


## -description



			The 
<b>NotifyAddrChange</b> function causes a notification to be sent to the caller whenever a change occurs in the table that maps IPv4 addresses to interfaces.


## -parameters




### -param Handle [out]

A pointer to a <b>HANDLE</b> variable that receives a file handle for use in a subsequent call to the <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function. 

<div class="alert"><b>Warning</b>  Do not close this handle, and do not associate it with a completion port.</div>
<div> </div>

### -param overlapped [in]

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that  notifies the caller of any changes in the table that maps IP addresses to interfaces.


## -returns




						If the function succeeds, the return value is NO_ERROR if the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters. If the caller specifies non-<b>NULL</b> parameters, the return value for success is ERROR_IO_PENDING.

If the function fails, use 
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
<b>NotifyAddrChange</b> function may be called in two ways:<ul>
<li>Synchronous method</li>
<li>Asynchronous method</li>
</ul>


If the caller specifies <b>NULL</b> for the <i>Handle</i> and <i>overlapped</i> parameters, the call to 
<b>NotifyAddrChange</b> is synchronous and will block until an IP address change occurs. In this case if a change occurs, the <b>NotifyAddrChange</b> function completes to indicate that a change has occurred. 

If the <b>NotifyAddrChange</b> function is called synchronously, a notification will be sent on the next IPv4 address change until the application terminates. 

If the caller specifies a handle variable and an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, then the <b>NotifyAddrChange</b> function call is asynchronous and the caller can use the returned handle with the <b>OVERLAPPED</b> structure to receive asynchronous notification of IPv4 address changes using the <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function. See the following topics for information about using the handle and 
<b>OVERLAPPED</b> structure to receive notifications:

<ul>
<li>
<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>
</li>
</ul>
The <a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a> function cancels notification of IPv4 address and route changes previously requested with successful calls to the <b>NotifyAddrChange</b> or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a> functions.

Once an application has been notified of a change, the application can then call the <a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a> or <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function to retrieve the table of IPv4 addresses to determine what has changed. If the application is notified and requires notification for the next change, then the <b>NotifyAddrChange</b> function must be called again.

If the <b>NotifyAddrChange</b> function is called asynchronously, a notification will be sent on the next IPv4 address change until either the application cancels the notification by calling the <a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a> function or the application terminates. If the application terminates, the system will automatically cancel the registration for the notification. It is still recommended that an application explicitly cancel any notification before it terminates.  

Any registration for a notification does not persist across a system shut down or reboot.

On Windows Vista and later, the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568805">NotifyIpInterfaceChange</a> function  can be used to  register to be notified for changes to IPv4 and IPv6 interfaces on  the local computer.


#### Examples

The following example waits for a change to occur in the table that maps IP addresses to interfaces.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;windows.h&gt;

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

void main()
{
  OVERLAPPED overlap;
  DWORD ret;
    
  HANDLE hand = NULL;
  overlap.hEvent = WSACreateEvent();

  ret = NotifyAddrChange(&amp;hand, &amp;overlap);

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/10795401-003f-45ce-80f1-ccc31659298a">CancelIPChangeNotify</a>



<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568805">NotifyIpInterfaceChange</a>



<a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

