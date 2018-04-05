---
UID: NF:iphlpapi.EnableRouter
title: EnableRouter function
author: windows-driver-content
description: The EnableRouter function turns on IPv4 forwarding on the local computer. EnableRouter also increments a reference count that tracks the number of requests to enable IPv4 forwarding.
old-location: iphlp\enablerouter.htm
old-project: IpHlp
ms.assetid: 779f5840-d58d-4194-baa7-2c6a7aeb7d79
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: EnableRouter, EnableRouter function [IP Helper], _iphlp_enablerouter, iphlp.enablerouter, iphlpapi/EnableRouter
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
-	EnableRouter
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# EnableRouter function


## -description


The 
<b>EnableRouter</b> function turns on IPv4 forwarding on the local computer. 
<b>EnableRouter</b> also increments a reference count that tracks the number of requests to enable IPv4 forwarding.


## -parameters




### -param pHandle

A pointer to a handle. This parameter is currently unused.


### -param pOverlapped

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure should be set to zero. The <b>hEvent</b> member should contain a handle to a valid event object. Use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function to create this event object.


## -returns



If the <b>EnableRouter</b> function succeeds, the return value is ERROR_IO_PENDING.

If the function fails, use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid. This error is returned if the <i>pOverlapped</i> parameter is <b>NULL</b>.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>EnableRouter</b> function is specific to IPv4 forwarding. If the process that calls 
<b>EnableRouter</b> terminates without calling 
<a href="https://msdn.microsoft.com/95f0387f-24e8-4382-b78e-e59bcec0f2ed">UnenableRouter</a>, the system  decrements the reference count that tracks the number of requests to enable IPv4 forwarding as though the process had called 
<b>UnenableRouter</b>. 




## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/95f0387f-24e8-4382-b78e-e59bcec0f2ed">UnenableRouter</a>
 

 

