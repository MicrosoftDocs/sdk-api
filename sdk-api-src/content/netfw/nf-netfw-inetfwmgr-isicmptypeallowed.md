---
UID: NF:netfw.INetFwMgr.IsIcmpTypeAllowed
title: INetFwMgr::IsIcmpTypeAllowed
author: windows-sdk-content
description: Determines whether the specified ICMP type is allowed.
old-location: ics\inetfwmgr_isicmptypeallowed.htm
old-project: ics
ms.assetid: 9ff5ef3b-581e-4ce5-9424-dafb08cfe067
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INetFwMgr interface [ICS/ICF],IsIcmpTypeAllowed method, INetFwMgr.IsIcmpTypeAllowed, INetFwMgr::IsIcmpTypeAllowed, IsIcmpTypeAllowed, IsIcmpTypeAllowed method [ICS/ICF], IsIcmpTypeAllowed method [ICS/ICF],INetFwMgr interface, ics.inetfwmgr_isicmptypeallowed, netfw/INetFwMgr::IsIcmpTypeAllowed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwMgr.IsIcmpTypeAllowed
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

