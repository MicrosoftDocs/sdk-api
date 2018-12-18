---
UID: NF:netioapi.GetIpInterfaceEntry
title: GetIpInterfaceEntry function
author: windows-sdk-content
description: Retrieves IP information for the specified interface on the local computer.
old-location: iphlp\getipinterfaceentry.htm
tech.root: IpHlp
ms.assetid: 604e33fd-ab12-4861-a083-544045f46ef4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIpInterfaceEntry, GetIpInterfaceEntry function [IP Helper], iphlp.getipinterfaceentry, netioapi/GetIpInterfaceEntry
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpInterfaceEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIpInterfaceEntry function


## -description


The 
<b>GetIpInterfaceEntry</b> function  retrieves IP information for the specified interface on the local computer.


## -parameters




### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure that, on successful return, receives information for an interface on the local computer. On input, the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <b>MIB_IPINTERFACE_ROW</b> must be set to the interface for which to retrieve information.


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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> pointed to by the <i>Row</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Family</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> pointed to by the <i>Row</i> parameter was not specified as <b>AF_INET</b> or <b>AF_INET6</b>, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPINTERFACE_ROW</b> pointed to by the <i>Row</i> parameter were unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure pointed to by the <i>Row</i> parameter does not match the IP address family specified in the <b>Family</b> member in the <b>MIB_IPINTERFACE_ROW</b> structure.

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
the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetIpInterfaceEntry</b> function is defined on Windows Vista and later. 

On input, the <b>Family</b> member in the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to either <b>AF_INET</b> or <b>AF_INET6</b>. In addition on input, at least one of the following members in the <b>MIB_IPINTERFACE_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output, the <b>InterfaceLuid</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure pointed to by the <i>Row</i> parameter is filled in if the <b>InterfaceIndex</b> was specified. The other members of <b>MIB_IPINTERFACE_ROW</b> structure pointed to by the <i>Row</i> parameter are also filled in.

The <a href="https://msdn.microsoft.com/5e7aed65-63e1-4e7b-bccf-9a2485212432">InitializeIpInterfaceEntry</a> function must be used to initialize the fields of a
    <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure entry with default values.  An application can then change the
    fields in the <b>MIB_IPINTERFACE_ROW</b> entry it wishes to modify, and then call the <a href="https://msdn.microsoft.com/8e6d2c14-29c3-47a7-9eb8-0989df9da68c">SetIpInterfaceEntry</a> function.

Unprivileged simultaneous access to multiple networks of different security requirements creates a security hole and allows an unprivileged application to accidentally relay data between the two networks. A typical example is simultaneous access to a virtual private network (VPN) and the Internet. Windows Server 2003 and Windows XP use a weak host model, where RAS prevents such simultaneous access by increasing the route metric of all default routes over other interfaces. Thus all traffic is routed through the VPN interface, disrupting other network connectivity. 

On Windows Vista and later, a strong host model is used by default. If a source IP address is specified in the route lookup using <a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a> or <a href="https://msdn.microsoft.com/5e507d14-f603-467d-9c37-bb048658d0b1">GetBestRoute</a>, the route lookup is restricted to the interface of the source IP address. The route metric modification by RAS has no effect as the list of potential routes does not even have the route for the VPN interface thereby allowing traffic to the Internet. The <b>DisableDefaultRoutes</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> can be used to disable using the default route on an interface. This member can be used as a security measure by VPN clients to restrict split tunneling when split tunneling is not required by the VPN client. A VPN client can call the <a href="https://msdn.microsoft.com/8e6d2c14-29c3-47a7-9eb8-0989df9da68c">SetIpInterfaceEntry</a> function to set the <b>DisableDefaultRoutes</b> member to <b>TRUE</b> when required. A VPN client can query the current state of the <b>DisableDefaultRoutes</b> member by calling  the <b>GetIpInterfaceEntry</b> function. 




## -see-also




<a href="https://msdn.microsoft.com/5e507d14-f603-467d-9c37-bb048658d0b1">GetBestRoute</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/da787dae-5e89-4bf2-a9b6-90e727995414">GetIfEntry2</a>



<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/09f2bbff-3281-41ae-878f-61c5afa20ec5">GetIpInterfaceTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a>



<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a>



<a href="https://msdn.microsoft.com/c4bbb949-5573-42cd-bb03-e308ac40d569">MIB_IPINTERFACE_TABLE</a>



<a href="https://msdn.microsoft.com/8e6d2c14-29c3-47a7-9eb8-0989df9da68c">SetIpInterfaceEntry</a>
 

 

