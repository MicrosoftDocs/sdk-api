---
UID: NF:iphlpapi.GetBestInterface
title: GetBestInterface function
author: windows-sdk-content
description: The GetBestInterface function retrieves the index of the interface that has the best route to the specified IPv4 address.
old-location: iphlp\getbestinterface.htm
old-project: IpHlp
ms.assetid: 9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetBestInterface, GetBestInterface function [IP Helper], _iphlp_getbestinterface, iphlp.getbestinterface, iphlpapi/GetBestInterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetBestInterface
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetBestInterface function


## -description



			The 
<b>GetBestInterface</b> function retrieves the index of the interface that has the best route to the specified IPv4 address.


## -parameters




### -param dwDestAddr [in]

The destination IPv4 address for which to retrieve the interface that has the best route, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure.


### -param pdwBestIfIndex [out]

A pointer to a <b>DWORD</b> variable that receives the index of the interface that has the best route to the IPv4 address specified by <i>dwDestAddr</i>. 


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pdwBestIfIndex</i> parameter or if the <i>pdwBestIfIndex</i> points to memory that cannot be written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetBestInterface</b> function only works with IPv4 addresses. For use with IPv6 addresses, the <a href="https://msdn.microsoft.com/cfd1108e-d7a0-4fe5-be3f-299189089d37">GetBestInterfaceEx</a> must be used. 

For information about the <b>IPAddr</b> data type, see 
<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a> and 
<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions.

On Windows Vista and later, the <i>pdwBestIfIndex</i> parameter is treated internally by IP Helper as a pointer to a <b>NET_IFINDEX</b> datatype. 




## -see-also




<a href="https://msdn.microsoft.com/cfd1108e-d7a0-4fe5-be3f-299189089d37">GetBestInterfaceEx</a>



<a href="https://msdn.microsoft.com/5e507d14-f603-467d-9c37-bb048658d0b1">GetBestRoute</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>



<a href="_mpr_mib_best_if">MIB_BEST_IF</a>



<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>
 

 

