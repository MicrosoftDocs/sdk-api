---
UID: NF:iphlpapi.GetIpNetTable
title: GetIpNetTable function (iphlpapi.h)
author: windows-sdk-content
description: The GetIpNetTable function retrieves the IPv4 to physical address mapping table.
old-location: iphlp\getipnettable.htm
tech.root: IpHlp
ms.assetid: 01bcf86e-5fcc-4ce9-bb89-02d393e75d1d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIpNetTable, GetIpNetTable function [IP Helper], _iphlp_getipnettable, iphlp.getipnettable, iphlpapi/GetIpNetTable
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
 - GetIpNetTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetIpNetTable function


## -description


The 
<b>GetIpNetTable</b> function retrieves the IPv4 to physical address mapping table.


## -parameters




### -param IpNetTable [out]

A pointer to a buffer that receives the IPv4 to physical address mapping table as a 
<a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a> structure.


### -param SizePointer [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>pIpNetTable</i> parameter.

On output, if the buffer is not large enough to hold the returned mapping table, the function sets this parameter equal to the required buffer size in bytes.


### -param Order [in]

A Boolean value that specifies whether the returned mapping table should be sorted in ascending order by IP address. If this parameter is <b>TRUE</b>, the table is sorted.


## -returns



If the function succeeds, the return value is NO_ERROR or ERROR_NO_DATA.

If the function fails or does not return any data, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pIpNetTable</i> parameter is not large enough. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>pdwSize</i> parameter is <b>NULL</b>, or 
<a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
There is no data to return. The IPv4 to physical address mapping table is empty. This return value indicates that the call to the <a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a> function succeeded, but there was no data to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 transport is not configured on the local computer.

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



The  
<b>GetIpNetTable</b> function enumerates the Address Resolution Protocol (ARP) entries for IPv4 on a local system from the IPv4 to physical address mapping table and returns this information in a <a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a> structure. 

The IPv4 address entries are returned in a <a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a> structure in the buffer pointed to by the <i>pIpNetTable</i> parameter. The <b>MIB_IPNETTABLE</b> structure contains a count of ARP entries and an array of <a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a> structures for each IPv4 address entry. 

Note that the returned <a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a> structure pointed to by the <i>pIpNetTable</i> parameter may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a> array entry in the <b>table</b> member of the <b>MIB_IPNETTABLE</b> structure. Padding for alignment may also be present between the <b>MIB_IPNETROW</b> array entries. Any access to a <b>MIB_IPNETROW</b> array entry should assume  padding may exist. 



 on Windows Vista and later, the <a href="https://msdn.microsoft.com/6c45d735-9a07-41ca-8d8a-919f32c98a3c">GetIpNetTable2</a> function can be used to retrieve the neighbor IP addresses for both IPv6 and IPv4. 




## -see-also




<a href="https://msdn.microsoft.com/607f9aad-2046-4ab2-9a62-4092f87ffa66">CreateIpNetEntry</a>



<a href="https://msdn.microsoft.com/0d338676-b66f-410c-8022-5576096954b4">DeleteIpNetEntry</a>



<a href="https://msdn.microsoft.com/cf4dea10-552d-4730-a452-9302ef3761ff">FlushIpNetTable</a>



<a href="https://msdn.microsoft.com/6c45d735-9a07-41ca-8d8a-919f32c98a3c">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a>



<a href="https://msdn.microsoft.com/1cac1c19-bc42-4aee-b9d0-d007b8798eeb">MIB_IPNETTABLE</a>



<a href="https://msdn.microsoft.com/d985b749-5aa3-4b4a-ba8f-bc8edcf1b1f3">SetIpNetEntry</a>
 

 

