---
UID: NF:dhcpsapi.DhcpEnumClassesV6
title: DhcpEnumClassesV6 function
author: windows-sdk-content
description: Enumerates the user or vendor classes configured for the DHCPv6 server.
old-location: dhcp\dhcpenumclassesv6.htm
tech.root: DHCP
ms.assetid: 3b916df3-ae17-4e7d-9cbc-d70763a8b856
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpEnumClassesV6, DhcpEnumClassesV6 function [DHCP], dhcp.dhcpenumclassesv6, dhcpsapi/DhcpEnumClassesV6
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpEnumClassesV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpEnumClassesV6 function


## -description


The <b>DhcpEnumClassesV6</b> function enumerates the  user or vendor classes configured for the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCPv6 server.


### -param ReservedMustBeZero [in]

Reserved. This field must be set to zero.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100 classes, and 200 classes are stored on the server, the resume handle can be used after the first 100 classes are retrieved to obtain the next 100 on a subsequent call, and so forth.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of classes to return. If the number of remaining unenumerated classes is less than this value, then that amount will be returned. To retrieve all classes available on the DHCPv6 server, set this parameter to 0xFFFFFFFF.


### -param ClassInfoArray [out]

Pointer to a  <a href="https://msdn.microsoft.com/b724ae08-4e18-4cad-9376-174acbd5b4f7">DHCP_CLASS_INFO_ARRAY_V6</a> structure that contains the returned classes. If there are no classes available on the DHCP server, this parameter will return null.


### -param nRead [out]

Pointer to a DWORD value that specifies the number of classes returned in <i>ClassInfoArray</i>.


### -param nTotal [out]

Pointer to a DWORD value that specifies the total number of classes stored on the DHCP server.


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
</table>
 




## -remarks



The caller of this function must free the memory pointed to by <i>ClassInfoArray</i>.




## -see-also




<a href="https://msdn.microsoft.com/b724ae08-4e18-4cad-9376-174acbd5b4f7">DHCP_CLASS_INFO_ARRAY_V6</a>



<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a>
 

 

