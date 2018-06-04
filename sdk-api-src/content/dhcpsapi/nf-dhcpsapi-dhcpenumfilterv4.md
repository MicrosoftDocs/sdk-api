---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DhcpEnumFilterV4 function


## -description


The <b>DhcpEnumFilterV4</b> function enumerates all of the filter records from the DHCP server's allow or deny list.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a> structure that identifies the enumeration operation. Initially this parameter must be set to zero (0), with a successful call returning the address/pattern value used for subsequent enumeration requests.


### -param PreferredMaximum [in]

A DWORD value that specifies the preferred maximum number of bytes to return. If the number of remaining unenumerated filter information size is less than this value, then all the filters configured on the particular list on the DHCP server are returned. The maximum value for this is 64 (kilobytes), and the minimum value is 1 (kilobyte).


### -param ListType [in]

A <a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a> that specifies the list of filters to be enumerated.


### -param EnumFilterInfo [out]

Pointer to the address of an array of <a href="https://msdn.microsoft.com/f393987c-12dd-468c-98c6-84f4d36744b2">DHCP_FILTER_ENUM_INFO</a> structures that contain the returned link-layer filter information configured on the DHCP server.


### -param ElementsRead [out]

Pointer to a <b>DWORD</b> value that specifies the number of link-layer filter entries returned in <i>EnumFilterInfo</i>.


### -param ElementsTotal [out]

Pointer to a <b>DWORD</b> value that specifies the number of link-layer filter entries defined on the DHCP server that have not yet been enumerated.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements available for enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f393987c-12dd-468c-98c6-84f4d36744b2">DHCP_FILTER_ENUM_INFO</a>



<a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a>
 

 

