---
UID: NF:iphlpapi.DeletePersistentUdpPortReservation
title: DeletePersistentUdpPortReservation function (iphlpapi.h)
description: Deletes a persistent TCP port reservation for a consecutive block of TCP ports on the local computer. (DeletePersistentUdpPortReservation)
helpviewer_keywords: ["DeletePersistentUdpPortReservation","DeletePersistentUdpPortReservation function [IP Helper]","iphlp.deletepersistentudpportreservation","iphlpapi/DeletePersistentUdpPortReservation"]
old-location: iphlp\deletepersistentudpportreservation.htm
tech.root: IpHlp
ms.assetid: E6539B3F-48DA-41AA-8AD4-2EBBAF98069F
ms.date: 12/05/2018
ms.keywords: DeletePersistentUdpPortReservation, DeletePersistentUdpPortReservation function [IP Helper], iphlp.deletepersistentudpportreservation, iphlpapi/DeletePersistentUdpPortReservation
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeletePersistentUdpPortReservation
 - iphlpapi/DeletePersistentUdpPortReservation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - DeletePersistentUdpPortReservation
---

# DeletePersistentUdpPortReservation function


## -description

The 
<b>DeletePersistentUdpPortReservation</b> function deletes a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting UDP port number in network byte order.

### -param NumberOfPorts [in]

The number of UDP port numbers to delete.

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
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element was not found. This error is returned if persistent port block specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters could not be found. 

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>DeletePersistentUdpPortReservation</b> function is defined on Windows Vista and later. 

The <b>DeletePersistentUdpPortReservation</b> function is used to delete a persistent reservation for a block of UDP ports. 

The <b>DeletePersistentUdpPortReservation</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeletePersistentUdpPortReservation</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation">DeletePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>
