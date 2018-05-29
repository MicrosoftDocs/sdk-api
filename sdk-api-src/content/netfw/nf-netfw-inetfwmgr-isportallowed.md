---
UID: NF:netfw.INetFwMgr.IsPortAllowed
title: INetFwMgr::IsPortAllowed
author: windows-sdk-content
description: Determines whether an application can listen for inbound traffic on the specified port.
old-location: ics\inetfwmgr_isportallowed.htm
old-project: ICS
ms.assetid: 39e68271-8046-470a-af90-17bed770716d
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: INetFwMgr interface [ICS/ICF],IsPortAllowed method, INetFwMgr.IsPortAllowed, INetFwMgr::IsPortAllowed, IsPortAllowed, IsPortAllowed method [ICS/ICF], IsPortAllowed method [ICS/ICF],INetFwMgr interface, ics.inetfwmgr_isportallowed, netfw/INetFwMgr::IsPortAllowed
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
-	Hnetcfg.dll
api_name:
-	INetFwMgr.IsPortAllowed
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwMgr::IsPortAllowed


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Determines whether an application can listen for inbound traffic on the
   specified port.


## -parameters




### -param imageFileName [in]

The image file name of the process listening on the
   network. It must be a fully qualified path, but  may contain
   environment variables. If <i>imageFileName</i> is <b>NULL</b>, the function
   determines whether the port is allowed for all applications.


### -param ipVersion [in]

IP version of the traffic. If <i>localAddress</i> is non-<b>NULL</b>,
   this must not be <b>NET_FW_IP_VERSION_ANY</b>.


### -param portNumber [in]

Local IP port number of the traffic. 


### -param localAddress [in]

Either a dotted-decimal IPv4 address or an IPv6 hex
   address specifying the local address of the traffic. Typically, this is
   the address passed to bind. If <i>localAddress</i> is <b>NULL</b>, the function
   determines whether the port is allowed for all interfaces.


### -param ipProtocol [in]

IP protocol of the traffic, either <b>NET_FW_IP_PROTOCOL_TCP</b> or <b>NET_FW_IP_PROTOCOL_UDP</b>.


### -param allowed [out]

Indicates by a value of VARIANT_TRUE or VARIANT_FALSE whether the port is allowed for at least some local
   interfaces and remote addresses.


### -param restricted [out]

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
If the method succeeds, the return value is S_OK.

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

The  <b>IsPortAllowed</b> method checks whether traffic will be allowed with the current firewall configuration for:



<ul>
<li>A specific application. 
</li>
<li>A specific port. 
</li>
<li>A specific application on a specific port.</li>
</ul>
 
 

In its operation <b>IsPortAllowed</b> considers whether the firewall is currently enabled or disabled, whether the application is allowed in the current profile Exceptions List, whether the port is allowed in the current profile Exceptions List, whether the file and print sharing option has been enabled, and whether the remote administration option has been enabled.


Because of the many factors in determining whether a port is allowed, the more specific information that is given via this method's input parameters, the more likely  a clear result with meaningful restrictions will be returned.




## -see-also




<a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a>



<a href="https://msdn.microsoft.com/867a038c-ae8e-4da8-a3e9-3ca7cb6ba518">NET_FW_IP_PROTOCOL</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

