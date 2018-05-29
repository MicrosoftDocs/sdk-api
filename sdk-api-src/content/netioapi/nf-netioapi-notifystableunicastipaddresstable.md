---
UID: NF:netioapi.NotifyStableUnicastIpAddressTable
title: NotifyStableUnicastIpAddressTable function
author: windows-sdk-content
description: Retrieves the stable unicast IP address table on a local computer.
old-location: iphlp\notifystableunicastipaddresstable.htm
old-project: IpHlp
ms.assetid: 80d10088-79ef-41fd-add7-994d2a780ddb
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, NotifyStableUnicastIpAddressTable, NotifyStableUnicastIpAddressTable function [IP Helper], iphlp.notifystableunicastipaddresstable, netioapi/NotifyStableUnicastIpAddressTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	NotifyStableUnicastIpAddressTable
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NotifyStableUnicastIpAddressTable function


## -description


The 
<b>NotifyStableUnicastIpAddressTable</b> function  retrieves the stable unicast IP address table on  a local computer.


## -parameters




### -param Family [in]

The address family to retrieve. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  the function  retrieves the stable unicast IP address table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  the function retrieves the stable unicast IP address table containing only IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  the function retrieves the stable unicast IP address table containing only IPv6 entries. 

</td>
</tr>
</table>
 


### -param Table [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a> structure. When <b>NotifyStableUnicastIpAddressTable</b> is successful, this parameter returns the stable unicast IP address table on the local computer.  

When <b>NotifyStableUnicastIpAddressTable</b> returns <b>ERROR_IO_PENDING</b> indicating that the I/O request is pending, then the  stable unicast IP address table is returned to the function in the <i>CallerCallback</i>  parameter.


### -param CallerCallback [in]

A pointer to the function to call with the stable unicast IP address table. This function will be invoked
        if <b>NotifyStableUnicastIpAddressTable</b> returns <b>ERROR_IO_PENDING</b>, indicating that the I/O request is pending. 


### -param CallerContext [in]

A user context passed to the callback function specified in the <i>CallerCallback</i> parameter when the stable unicast IP address table si available.


### -param NotificationHandle [in, out]

A pointer used to return a handle that can be used to
        cancel the request to retrieve the stable unicast IP address table. This parameter is returned if  the return value from <b>NotifyStableUnicastIpAddressTable</b> is <b>ERROR_IO_PENDING</b> indicating that the I/O request is pending. 


## -returns



If the function succeeds immediately, the return value is NO_ERROR and the stable unicast IP table is returned in the <i>Table</i> parameter.

If the I/O request is pending, the function returns <b>ERROR_IO_PENDING</b> and the function pointed to by the <i>CallerCallback</i> parameter is called when the I/O request has completed with the stable unicast IP address table.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred where an invalid handle was encountered. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>Table</i> parameter was  a <b>NULL</b> pointer, the <i>NotificationHandle</i> parameter was  a <b>NULL</b> pointer,  or the <i>Family</i> parameter was not either <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY
</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory.

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



The <b>NotifyStableUnicastIpAddressTable</b> function is defined on Windows Vista and later. 

If the <b>NotifyStableUnicastIpAddressTable</b> function succeeds immediately, the return value is NO_ERROR and the stable unicast IP table is returned in the <i>Table</i> parameter.  The calling application should free the memory pointed to by the <i>Table</i> parameter using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a> function when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a> information is no longer needed.

All unicast IP addresses except dial-on-demand addresses are considered stable only if they are in the preferred state.  For a normal unicast IP address entry, this would correspond to a DadState member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> for the IP address set to <b>IpDadStatePreferred</b>. 
Every dial-on-demand address defines its own stability metric.  Currently the only dial-on-demand address considered by this function is the unicast IP address used by the Teredo client on the local computer. 

The <i>Family</i> parameter must be set to either <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

When <b>NotifyStableUnicastIpAddressTable</b> is successful and returns NO_ERROR, the <i>Table</i> parameter returns the stable unicast IP address table on the local computer. 

When <b>NotifyStableUnicastIpAddressTable</b> returns <b>ERROR_IO_PENDING</b> indicating that the I/O request is pending, then the  stable unicast IP address table is returned to the function in the <i>CallerCallback</i>  parameter.

The <b>NotifyStableUnicastIpAddressTable</b> function is used primarily by applications that use the Teredo client.

If the unicast IP address used by Teredo is available on the local computer but not in the stable (qualified) state, <b>NotifyStableUnicastIpAddressTable</b> returns ERROR_IO_PENDING and the stable unicast IP address table is eventually returned by  calling the function in the <i>CallerCallback</i>  parameter.  If the Teredo address is not available or is in the stable state and the other unicast IP addresses are in a stable state, then the function  in the <i>CallerCallback</i>  parameter will never be invoked.  

The callback function specified in the <i>CallerCallback</i> parameter should be defined as a function of type <b>VOID</b>. The parameters passed to the callback function include the following:

<table>
<tr>
<th>Parameter</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="IN_PVOID_CallerContext"></a><a id="in_pvoid_callercontext"></a><a id="IN_PVOID_CALLERCONTEXT"></a>IN PVOID CallerContext

</td>
<td width="60%">
The <i>CallerContext</i> parameter passed to the <b>NotifyStableUnicastIpAddressTable</b> function when registering for notifications.

</td>
</tr>
<tr>
<td width="40%">
<a id="IN_PMIB_UNICASTIPADDRESS_TABLE_AddressTable"></a><a id="in_pmib_unicastipaddress_table_addresstable"></a><a id="IN_PMIB_UNICASTIPADDRESS_TABLE_ADDRESSTABLE"></a>IN PMIB_UNICASTIPADDRESS_TABLE AddressTable

</td>
<td width="60%">
A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a> containing the stable unicast IP address table on the local computer. 

</td>
</tr>
</table>
 



The callback function specified in the <i>CallerCallback</i> parameter must be implemented in the same process as the application calling the <b>NotifyStableUnicastIpAddressTable</b> function. If the callback function is in a separate DLL, then the DLL should be loaded before calling the <b>NotifyStableUnicastIpAddressTable</b> function to register for change notifications. 

The memory pointed to by the <i>AddressTable</i> parameter used in a callback indication is alocated by the operating system. An application that receives a notification should free the memory pointed to by the <i>AddressTable</i> parameter using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a> function when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a> information is no longer needed. 

Once the <b>NotifyStableUnicastIpAddressTable</b> function is called to register for change notifications, these notifications will continue to be sent until the application deregisters for change notifications or the application terminates. If the application terminates, the system will automatically deregister any registration for change notifications. It is still recommended that an application explicitly deregister any change notifications before it terminates.  

Any registration for change notifications does not persist if the system is shutdown or rebooted. 

To deregister for change notifications, call the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff544864">CancelMibChangeNotify2</a> function passing the <i>NotificationHandle</i> parameter returned by  <b>NotifyStableUnicastIpAddressTable</b>. 

An application cannot make a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544864">CancelMibChangeNotify2</a> function from the context of the thread which is currently executing the notification callback function for the same <i>NotificationHandle</i> parameter. Otherwise, the thread executing that callback will result in deadlock. So the <b>CancelMibChangeNotify2</b> function must not be called directly as part of the notification callback routine. In a more general situation, a thread that executes the <b>CancelMibChangeNotify2</b> function cannot own a resource on which the thread that executes a notification callback operation would wait because it would result in a similar deadlock. The <b>CancelMibChangeNotify2</b> function should be called from a different thread, on which the thread that receives the notification callback doesn’t have dependencies on.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544864">CancelMibChangeNotify2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546227">CreateUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546370">DeleteUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552578">GetTeredoPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552589">GetUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552594">GetUnicastIpAddressTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554886">InitializeUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559286">MIB_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568808">NotifyTeredoPortChange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568809">NotifyUnicastIpAddressChange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570800">SetUnicastIpAddressEntry</a>
 

 

