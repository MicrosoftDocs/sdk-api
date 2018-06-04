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

# _DHCPV6CAPI_PARAMS structure


## -description


A <b>DHCPV6CAPI_PARAMS</b> structure contains a requested parameter.


## -struct-fields




### -field Flags

Reserved for future use.


### -field OptionId

Identifier for the DHCPv6 parameter being requested.

<a id="DHCPV6_OPTION_CLIENTID"></a>
<a id="dhcpv6_option_clientid"></a>


#### DHCPV6_OPTION_CLIENTID

<a id="DHCPV6_OPTION_SERVERID"></a>
<a id="dhcpv6_option_serverid"></a>


#### DHCPV6_OPTION_SERVERID

<a id="DHCPV6_OPTION_IA_NA"></a>
<a id="dhcpv6_option_ia_na"></a>


#### DHCPV6_OPTION_IA_NA

<a id="DHCPV6_OPTION_IA_TA"></a>
<a id="dhcpv6_option_ia_ta"></a>


#### DHCPV6_OPTION_IA_TA

<a id="DHCPV6_OPTION_ORO"></a>
<a id="dhcpv6_option_oro"></a>


#### DHCPV6_OPTION_ORO

<a id="DHCPV6_OPTION_PREFERENCE"></a>
<a id="dhcpv6_option_preference"></a>


#### DHCPV6_OPTION_PREFERENCE

<a id="DHCPV6_OPTION_UNICAST"></a>
<a id="dhcpv6_option_unicast"></a>


#### DHCPV6_OPTION_UNICAST

<a id="DHCPV6_OPTION_RAPID_COMMIT"></a>
<a id="dhcpv6_option_rapid_commit"></a>


#### DHCPV6_OPTION_RAPID_COMMIT

<a id="DHCPV6_OPTION_USER_CLASS"></a>
<a id="dhcpv6_option_user_class"></a>


#### DHCPV6_OPTION_USER_CLASS

<a id="DHCPV6_OPTION_VENDOR_CLASS"></a>
<a id="dhcpv6_option_vendor_class"></a>


#### DHCPV6_OPTION_VENDOR_CLASS

<a id="DHCPV6_OPTION_VENDOR_OPTS"></a>
<a id="dhcpv6_option_vendor_opts"></a>


#### DHCPV6_OPTION_VENDOR_OPTS

<a id="DHCPV6_OPTION_RECONF_MSG"></a>
<a id="dhcpv6_option_reconf_msg"></a>


#### DHCPV6_OPTION_RECONF_MSG

<a id="DHCPV6_OPTION_SIP_SERVERS_NAMES"></a>
<a id="dhcpv6_option_sip_servers_names"></a>


#### DHCPV6_OPTION_SIP_SERVERS_NAMES

<a id="DHCPV6_OPTION_SIP_SERVERS_ADDRS"></a>
<a id="dhcpv6_option_sip_servers_addrs"></a>


#### DHCPV6_OPTION_SIP_SERVERS_ADDRS

<a id="DHCPV6_OPTION_DNS_SERVERS"></a>
<a id="dhcpv6_option_dns_servers"></a>


#### DHCPV6_OPTION_DNS_SERVERS

<a id="DHCPV6_OPTION_DOMAIN_LIST"></a>
<a id="dhcpv6_option_domain_list"></a>


#### DHCPV6_OPTION_DOMAIN_LIST

<a id="DHCPV6_OPTION_IA_PD"></a>
<a id="dhcpv6_option_ia_pd"></a>


#### DHCPV6_OPTION_IA_PD

<a id="DHCPV6_OPTION_NIS_SERVERS"></a>
<a id="dhcpv6_option_nis_servers"></a>


#### DHCPV6_OPTION_NIS_SERVERS

<a id="DHCPV6_OPTION_NISP_SERVERS"></a>
<a id="dhcpv6_option_nisp_servers"></a>


#### DHCPV6_OPTION_NISP_SERVERS

<a id="DHCPV6_OPTION_NIS_DOMAIN_NAME"></a>
<a id="dhcpv6_option_nis_domain_name"></a>


#### DHCPV6_OPTION_NIS_DOMAIN_NAME

<a id="DHCPV6_OPTION_CLIENTIDNISP_DOMAIN_NAME"></a>
<a id="dhcpv6_option_clientidnisp_domain_name"></a>


#### DHCPV6_OPTION_CLIENTIDNISP_DOMAIN_NAME


### -field IsVendor

This option is set to <b>TRUE</b> if this parameter is vendor-specific.  Otherwise, it is <b>FALSE</b>.


### -field Data

Contains the actual parameter data.


### -field nBytesData

Size of the <b>Data</b> member, in bytes.

