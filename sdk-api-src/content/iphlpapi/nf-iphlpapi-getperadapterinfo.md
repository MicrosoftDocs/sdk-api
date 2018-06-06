---
UID: NF:iphlpapi.GetPerAdapterInfo
title: GetPerAdapterInfo function
author: windows-sdk-content
description: The GetPerAdapterInfo function retrieves information about the adapter corresponding to the specified interface.
old-location: iphlp\getperadapterinfo.htm
old-project: IpHlp
ms.assetid: fc1ae7e4-f856-4b48-8ab4-56cd511ed161
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetPerAdapterInfo, GetPerAdapterInfo function [IP Helper], _iphlp_getperadapterinfo, iphlp.getperadapterinfo, iphlpapi/GetPerAdapterInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetPerAdapterInfo
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetPerAdapterInfo function


## -description



			The 
<b>GetPerAdapterInfo</b> function retrieves information about the adapter corresponding to the specified interface.


## -parameters




### -param IfIndex [in]

Index of an interface. 
The <b>GetPerAdapterInfo</b> function retrieves information for the adapter corresponding to this interface.


### -param pPerAdapterInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/10cfdded-4184-4d34-9ccd-85446c13d497">IP_PER_ADAPTER_INFO</a> structure that receives information about the adapter.


### -param pOutBufLen [in]

Pointer to a <b>ULONG</b> variable that specifies the size of the 
<a href="https://msdn.microsoft.com/10cfdded-4184-4d34-9ccd-85446c13d497">IP_PER_ADAPTER_INFO</a> structure. If this size is insufficient to hold the information, 
<b>GetPerAdapterInfo</b> fills in this variable with the required size, and returns an error code of ERROR_BUFFER_OVERFLOW.


## -returns




						If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer size indicated by the <i>pOutBufLen</i> parameter is too small to hold the adapter information. The <i>pOutBufLen</i> parameter points to the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pOutBufLen</i> parameter is <b>NULL</b>, or the calling process does not have read/write access to the memory pointed to by <i>pOutBufLen</i>, or the calling process does not have write access to the memory pointed to by the <i>pAdapterInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/fc1ae7e4-f856-4b48-8ab4-56cd511ed161">GetPerAdapterInfo</a> is not supported by the operating system running on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



 An  adapter index  may change when the adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.




## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/10cfdded-4184-4d34-9ccd-85446c13d497">IP_PER_ADAPTER_INFO</a>
 

 

