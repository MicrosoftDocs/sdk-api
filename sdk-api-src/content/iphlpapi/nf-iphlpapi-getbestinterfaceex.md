---
UID: NF:iphlpapi.GetBestInterfaceEx
title: GetBestInterfaceEx function
author: windows-sdk-content
description: The GetBestInterfaceEx function retrieves the index of the interface that has the best route to the specified IPv4 or IPv6 address.
old-location: iphlp\getbestinterfaceex.htm
tech.root: IpHlp
ms.assetid: cfd1108e-d7a0-4fe5-be3f-299189089d37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBestInterfaceEx, GetBestInterfaceEx function [IP Helper], iphlp.getbestinterfaceex, iphlpapi/GetBestInterfaceEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - GetBestInterfaceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetBestInterfaceEx function


## -description


The 
<b>GetBestInterfaceEx</b> function retrieves the index of the interface that has the best route to the specified IPv4 or IPv6 address.


## -parameters




### -param pDestAddr [in]

The destination IPv6 or IPv4 address for which to retrieve the interface with the best route, in the form of a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure.


### -param pdwBestIfIndex [out]

A pointer to the index of the interface with the best route to the IPv6 or IPv4 address specified by <i>pDestAddr</i>.


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pdwBestIfIndex</i> parameter or if the <i>pDestAddr </i> or <i>pdwBestIfIndex</i> parameters point to memory that cannot be accessed. This error can also be returned if the <i>pdwBestIfIndex</i> parameter points to memory that can't be written to.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <i>pDestAddr</i> parameter or no IPv6 stack is on the local computer and an IPv6 address was specified in the <i>pDestAddr</i> parameter.

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



The <b>GetBestInterfaceEx</b> function differs from the <a href="https://msdn.microsoft.com/9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1">GetBestInterface</a> function in that it can be used with either IPv4 or IPv6 addresses.

The <b>Family</b> member of the sockaddr structure pointed to by the <i>pDestAddr</i> parameter must be set to one of the following values: <b>AF_INET</b> or <b>AF_INET6</b>. 

On Windows Vista and later, the <i>pdwBestIfIndex</i> parameter is treated internally by IP Helper as a pointer to a <b>NET_IFINDEX</b> datatype. 




## -see-also




<a href="https://msdn.microsoft.com/9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1">GetBestInterface</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366822(v=VS.85).aspx">MIB_BEST_IF</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a>
 

 

