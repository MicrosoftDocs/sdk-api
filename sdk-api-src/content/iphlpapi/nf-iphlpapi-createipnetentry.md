---
UID: NF:iphlpapi.CreateIpNetEntry
title: CreateIpNetEntry function
author: windows-sdk-content
description: The CreateIpNetEntry function creates an Address Resolution Protocol (ARP) entry in the ARP table on the local computer.
old-location: iphlp\createipnetentry.htm
old-project: iphlp
ms.assetid: 607f9aad-2046-4ab2-9a62-4092f87ffa66
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CreateIpNetEntry, CreateIpNetEntry function [IP Helper], _iphlp_createipnetentry, iphlp.createipnetentry, iphlpapi/CreateIpNetEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CreateIpNetEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreateIpNetEntry function


## -description


The 
<b>CreateIpNetEntry</b> function creates an Address Resolution Protocol (ARP) entry in the ARP table on the local computer.


## -parameters




### -param pArpEntry [in]

A pointer to a 
<a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a> structure that specifies information for the new entry. The caller must specify values for all members of this structure.


## -returns



The function returns <b>NO_ERROR</b> (zero) if the function is successful. 

If the function fails, the return value is one of the following error codes.

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
Access is denied. This error is returned on Windows Vista and Windows Server 2008 under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An input parameter is invalid, no action was taken. This error is returned if the <i>pArpEntry</i> parameter is <b>NULL</b>,  the  <b>dwPhysAddrLen</b> member of 
<a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a> is set to zero or a value greater than 8, the <b>&gt;dwAddr</b> member of the <b>MIB_IPNETROW</b> structure is invalid, or one of the other members of the 
<b>MIB_IPNETROW</b> structure is invalid. 

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



To modify an existing ARP entry, use the 
<a href="https://msdn.microsoft.com/d985b749-5aa3-4b4a-ba8f-bc8edcf1b1f3">SetIpNetEntry</a> function. To retrieve the ARP table, call the <a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a> function. To delete an existing ARP entry, call the <a href="https://msdn.microsoft.com/0d338676-b66f-410c-8022-5576096954b4">DeleteIpNetEntry</a>.

On Windows Vista and later, the <b>CreateIpNetEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateIpNetEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>CreateIpNetEntry</b> function can also fail because of user account control (UAC) on Windows Vista later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a0e90c0a-9403-40cb-906e-6e1e2f8e73c4">CreateProxyArpEntry</a>



<a href="https://msdn.microsoft.com/0d338676-b66f-410c-8022-5576096954b4">DeleteIpNetEntry</a>



<a href="https://msdn.microsoft.com/26e08e4d-ac69-49f8-8a1a-1ba1a04d085c">DeleteProxyArpEntry</a>



<a href="https://msdn.microsoft.com/cf4dea10-552d-4730-a452-9302ef3761ff">FlushIpNetTable</a>



<a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/aa9aa9f9-2334-4b08-896f-f4a77caa0f7f">MIB_IPNETROW</a>



<a href="https://msdn.microsoft.com/d985b749-5aa3-4b4a-ba8f-bc8edcf1b1f3">SetIpNetEntry</a>
 

 

