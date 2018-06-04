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

# INetFwMgr::IsIcmpTypeAllowed


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Determines whether the specified ICMP type is allowed.


## -parameters




### -param ipVersion [in]

IP version of the traffic. This cannot be <b>NET_FW_IP_VERSION_ANY</b>.

IP version of the traffic. 
   This cannot be <b>NET_FW_IP_VERSION_ANY</b>.


### -param localAddress [in]

Either a dotted-decimal IPv4 address or an IPv6 hex
   address specifying the local address of the traffic. Typically, this is
   the address passed to bind. If <i>localAddress</i> is <b>NULL</b>, the function
   determines whether the port is allowed for all interfaces.

Either a dotted-decimal IPv4 address or an IPv6 hex
   address specifying the local address of the traffic. Typically, this is
   the address passed to bind. If <i>localAddress</i> is <b>NULL</b>, the function
   determines whether the port is allowed for all interfaces.


### -param type [in]

ICMP type. For a list of possible ICMP types, see <a href="http://go.microsoft.com/fwlink/p/?linkid=109532">ICMP Type Numbers</a>.

ICMP type.


### -param allowed [out]

Indicates by a value of VARIANT_TRUE or VARIANT_FALSE whether the port is allowed for at least some local
   interfaces and remote addresses.

Indicates by a value of VARIANT_TRUE or VARIANT_FALSE whether the port is allowed for at least some local
   interfaces and remote addresses.


### -param restricted [out]

Indicates by a value of VARIANT_TRUE or VARIANT_FALSE whether some local interfaces or remote addresses
   are blocked for this port. For example, if the port is restricted to the
   local subnet only.

Indicates by a value of VARIANT_TRUE or VARIANT_FALSE whether some local interfaces or remote addresses
   are blocked for this port. For example, if the port is restricted to the
   local subnet only.


## -returns



<h3>C++</h3>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was stopped because of permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a parameter was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a pointer was not valid.

</td>
</tr>
</table>
 

<h3>VB</h3>

						If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was stopped because of permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a parameter was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a pointer was not valid.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/b6f27763-6ceb-4bc3-be6f-f02908dc0387">INetFwPolicy2::IsRuleGroupEnabled</a> method is generally recommended in place of this method.




## -see-also




<a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

