---
UID: NF:iphlpapi.GetRTTAndHopCount
title: GetRTTAndHopCount function
author: windows-driver-content
description: The GetRTTAndHopCount function determines the round-trip time (RTT) and hop count to the specified destination.
old-location: iphlp\getrttandhopcount.htm
old-project: IpHlp
ms.assetid: 4e84fe6f-40bd-4f0e-bb78-4180e13577aa
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetRTTAndHopCount, GetRTTAndHopCount function [IP Helper], _iphlp_getrttandhopcount, iphlp.getrttandhopcount, iphlpapi/GetRTTAndHopCount
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
-	GetRTTAndHopCount
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetRTTAndHopCount function


## -description



			The 
<b>GetRTTAndHopCount</b> function determines the round-trip time (RTT) and hop count to the specified destination.


## -parameters




### -param DestIpAddress [in]

IP address of the destination for which to determine the RTT and hop count, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure.


### -param HopCount [out]

Pointer to a <b>ULONG</b> variable. This variable receives the hop count to the destination specified by the <i>DestIpAddress</i> parameter.


### -param MaxHops [in]

Maximum number of hops to search for the destination. If the number of hops to the destination exceeds this number, the function terminates the search and returns <b>FALSE</b>.


### -param RTT [out]

Round-trip time, in milliseconds, to the destination specified by <i>DestIpAddress</i>.


## -returns




						If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to obtain the error code for the failure.




## -remarks



For information about the <b>IPAddr</b> data type, see 
<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a> and 
<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions.


#### Examples

The following example retrieves and prints the round trip time and hop count to the destination IP address 127.0.0.1.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>UINT ip = inet_addr("127.0.0.1");
ULONG hopCount = 0;
ULONG RTT = 0;

if(GetRTTAndHopCount(ip, &amp;hopCount, 30, &amp;RTT) == TRUE) {
  printf("Hops: %ld\n", hopCount);
  printf("RTT: %ld\n", RTT);
}
else {
  printf("Error: %ld\n", GetLastError());
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1">GetBestInterface</a>



<a href="https://msdn.microsoft.com/5e507d14-f603-467d-9c37-bb048658d0b1">GetBestRoute</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>
 

 

