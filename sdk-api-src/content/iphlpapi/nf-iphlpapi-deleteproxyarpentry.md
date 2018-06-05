---
UID: NF:iphlpapi.DeleteProxyArpEntry
title: DeleteProxyArpEntry function
author: windows-sdk-content
description: The DeleteProxyArpEntry function deletes the PARP entry on the local computer specified by the dwAddress and dwIfIndex parameters.
old-location: iphlp\deleteproxyarpentry.htm
old-project: IpHlp
ms.assetid: 26e08e4d-ac69-49f8-8a1a-1ba1a04d085c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: DeleteProxyArpEntry, DeleteProxyArpEntry function [IP Helper], _iphlp_deleteproxyarpentry, iphlp.deleteproxyarpentry, iphlpapi/DeleteProxyArpEntry
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
-	DeleteProxyArpEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# DeleteProxyArpEntry function


## -description


The 
<b>DeleteProxyArpEntry</b> function deletes the PARP entry on the local computer specified by the <i>dwAddress</i> and <i>dwIfIndex</i> parameters.


## -parameters




### -param dwAddress [in]

The IPv4 address for which this computer is acting as a proxy.


### -param dwMask [in]

The subnet mask for the IPv4 address specified in the <i>dwAddress</i> parameter.


### -param dwIfIndex [in]

The index of the interface on which this computer is supporting proxy ARP for the IP address specified by the <i>dwAddress</i> parameter.


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
An input parameter is invalid, no action was taken.  

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



To retrieve the ARP table, call the <a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a> function. 

On Windows Vista and later, the <b>DeleteProxyArpEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeleteProxyArpEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista and later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  This function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a0e90c0a-9403-40cb-906e-6e1e2f8e73c4">CreateProxyArpEntry</a>



<a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="_mpr_mib_proxyarp">MIB_PROXYARP</a>
 

 

