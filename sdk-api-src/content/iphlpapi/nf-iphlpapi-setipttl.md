---
UID: NF:iphlpapi.SetIpTTL
title: SetIpTTL function
author: windows-driver-content
description: The SetIpTTL function sets the default time-to-live (TTL) value for the local computer.
old-location: iphlp\setipttl.htm
old-project: IpHlp
ms.assetid: dfde8712-f68f-4fa4-b939-ea36e23b5b1e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: SetIpTTL, SetIpTTL function [IP Helper], _iphlp_setipttl, iphlp.setipttl, iphlpapi/SetIpTTL
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
-	SetIpTTL
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIpTTL function


## -description


The 
<b>SetIpTTL</b> function sets the default time-to-live (TTL) value for the local computer.


## -parameters




### -param nTTL [in]

The new TTL value for the local computer.


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
An invalid parameter was passed to the function. This error is returned if the  <i>nTTL</i> parameter is invalid. 

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



The default TTL can also be set using the 
<a href="https://msdn.microsoft.com/d857ee04-38b8-4d98-a3e7-6ca8657ac9ed">SetIpStatistics</a> function.

On Windows Vista and later, the <b>SetIpTTL</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIpTTL</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <a href="https://msdn.microsoft.com/d857ee04-38b8-4d98-a3e7-6ca8657ac9ed">SetIpStatistics</a> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>   On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a>



<a href="https://msdn.microsoft.com/d857ee04-38b8-4d98-a3e7-6ca8657ac9ed">SetIpStatistics</a>



<a href="https://msdn.microsoft.com/13b52016-5bdb-4546-af53-d3ae2708653b">SetIpStatisticsEx</a>
 

 

