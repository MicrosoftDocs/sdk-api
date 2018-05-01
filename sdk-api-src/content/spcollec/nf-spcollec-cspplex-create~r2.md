---
UID: NF:spcollec.CSPPlex.Create~r2
title: Create function
author: windows-driver-content
description: Creates the IPAddress.
old-location: nettcpip\create_msft_netipaddress.htm
old-project: NetTCPIPProv
ms.assetid: 5c4657fd-9cf6-4538-90ee-5aaa881e945b
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: 0, 1, 2, 23, 3, 4, 5, Create, Create method, Create method, MSFT_NetIPAddress class, MSFT_NetIPAddress class, Create method, MSFT_NetIPAddress.Create, nettcpip.create_msft_netipaddress, wmi.create_msft_netipaddress, wmi_v2.create_msft_netipaddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: spcollec.h
req.include-header: Dxtmpl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Root\StandardCimv2
req.assembly: 
req.type-library: 
req.typenames: SpatialAudioObjectRenderStreamForMetadataActivationParams
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	Create method of the MSFT_NetIPAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: NetTCPIP.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# Create function


## -description


Creates the IPAddress.


## -parameters




### -param pHead

TBD


### -param nMax

TBD


### -param cbElement

TBD




#### - AddressFamily [in]

Indicates whether the address family for this IP address is v4 or v6.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>IPv4</dt>
</dl>
</td>
<td width="60%">
The address family is IPv4

</td>
</tr>
<tr>
<td width="40%"><a id="23"></a><dl>
<dt><b>23</b></dt>
<dt>IPv6</dt>
</dl>
</td>
<td width="60%">
The address family is IPv6

</td>
</tr>
</table>
 


#### - AddressState [in]

Address lifetime state.



#### 0 (Invalid)



#### 1 (Tentative)



#### 2 (Duplicate)



#### 3 (Deprecated)



#### 4 (Preferred)


#### - CmdletOutput [out]

An embedded instance of the <a href="https://msdn.microsoft.com/a7dfa4b1-c89f-4e0e-9f96-82acf4780bf1">MSFT_NetIPAddress</a> class.


#### - DefaultGateway [in]

TBD


#### - IPAddress [in]

The IP address.


#### - InterfaceAlias [in]

The user-friendly interface name.


#### - InterfaceIndex [in]

The user-friendly interface index.


#### - PassThru [in]

Specifies whether the method should output an object that represents the newly created IP address in the <i>CmdletOutput</i> parameter.


#### - PolicyStore [in]

TBD


#### - PreferredLifetime [in]

Lifetime over which the address is preferred. The default value is infinite.


#### - PrefixLength [in]

The type of address.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>Unicast</dt>
</dl>
</td>
<td width="60%">
Marks the address as a unicast address. This is the default

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>Anycast</dt>
</dl>
</td>
<td width="60%">
Marks the address as an anycast address

</td>
</tr>
</table>
 


#### - PrefixOrigin [in]

Prefix origin of this address.



#### 0 (Other)



#### 1 (Manual)



#### 2 (WellKnown)



#### 3 (Dhcp)



#### 4 (RouterAdvertisement)


#### - SkipAsSource [in]

true to not use the address as source address for any outgoing packet unless explicitly asked to.


#### - SuffixOrigin [in]

Suffix origin of this address.



#### 0 (Other)



#### 1 (Manual)



#### 2 (WellKnown)



#### 3 (Dhcp)



#### 4 (Link)



#### 5 (Random)


#### - Type [in]

The type of address.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>Unicast</dt>
</dl>
</td>
<td width="60%">
Marks the address as a unicast address. This is the default

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>Anycast</dt>
</dl>
</td>
<td width="60%">
Marks the address as an anycast address

</td>
</tr>
</table>
 


#### - ValidLifetime [in]

Lifetime over which the address is valid. The default value is infinite.


## -see-also




<a href="https://msdn.microsoft.com/a7dfa4b1-c89f-4e0e-9f96-82acf4780bf1">MSFT_NetIPAddress</a>
 

 

