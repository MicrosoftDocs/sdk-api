---
UID: NS:dhcpv6csdk._DHCPV6CAPI_PARAMS
title: DHCPV6CAPI_PARAMS (dhcpv6csdk.h)
description: Contains a requested parameter.
helpviewer_keywords: ["*LPDHCPV6CAPI_PARAMS","*PDHCPV6CAPI_PARAMS","DHCPV6CAPI_PARAMS","DHCPV6CAPI_PARAMS structure [DHCP]","DHCPV6_OPTION_CLIENTID","DHCPV6_OPTION_CLIENTIDNISP_DOMAIN_NAME","DHCPV6_OPTION_DNS_SERVERS","DHCPV6_OPTION_DOMAIN_LIST","DHCPV6_OPTION_IA_NA","DHCPV6_OPTION_IA_PD","DHCPV6_OPTION_IA_TA","DHCPV6_OPTION_NISP_SERVERS","DHCPV6_OPTION_NIS_DOMAIN_NAME","DHCPV6_OPTION_NIS_SERVERS","DHCPV6_OPTION_ORO","DHCPV6_OPTION_PREFERENCE","DHCPV6_OPTION_RAPID_COMMIT","DHCPV6_OPTION_RECONF_MSG","DHCPV6_OPTION_SERVERID","DHCPV6_OPTION_SIP_SERVERS_ADDRS","DHCPV6_OPTION_SIP_SERVERS_NAMES","DHCPV6_OPTION_UNICAST","DHCPV6_OPTION_USER_CLASS","DHCPV6_OPTION_VENDOR_CLASS","DHCPV6_OPTION_VENDOR_OPTS","LPDHCPV6CAPI_PARAMS","LPDHCPV6CAPI_PARAMS structure pointer [DHCP]","PDHCPV6CAPI_PARAMS","PDHCPV6CAPI_PARAMS structure pointer [DHCP]","dhcp.dhcpv6capi_params","dhcpv6csdk/DHCPV6CAPI_PARAMS","dhcpv6csdk/LPDHCPV6CAPI_PARAMS","dhcpv6csdk/PDHCPV6CAPI_PARAMS"]
old-location: dhcp\dhcpv6capi_params.htm
tech.root: DHCP
ms.assetid: a8978435-a16d-446d-9bd3-4a2dc6c9ec1a
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6CAPI_PARAMS, *PDHCPV6CAPI_PARAMS, DHCPV6CAPI_PARAMS, DHCPV6CAPI_PARAMS structure [DHCP], DHCPV6_OPTION_CLIENTID, DHCPV6_OPTION_CLIENTIDNISP_DOMAIN_NAME, DHCPV6_OPTION_DNS_SERVERS, DHCPV6_OPTION_DOMAIN_LIST, DHCPV6_OPTION_IA_NA, DHCPV6_OPTION_IA_PD, DHCPV6_OPTION_IA_TA, DHCPV6_OPTION_NISP_SERVERS, DHCPV6_OPTION_NIS_DOMAIN_NAME, DHCPV6_OPTION_NIS_SERVERS, DHCPV6_OPTION_ORO, DHCPV6_OPTION_PREFERENCE, DHCPV6_OPTION_RAPID_COMMIT, DHCPV6_OPTION_RECONF_MSG, DHCPV6_OPTION_SERVERID, DHCPV6_OPTION_SIP_SERVERS_ADDRS, DHCPV6_OPTION_SIP_SERVERS_NAMES, DHCPV6_OPTION_UNICAST, DHCPV6_OPTION_USER_CLASS, DHCPV6_OPTION_VENDOR_CLASS, DHCPV6_OPTION_VENDOR_OPTS, LPDHCPV6CAPI_PARAMS, LPDHCPV6CAPI_PARAMS structure pointer [DHCP], PDHCPV6CAPI_PARAMS, PDHCPV6CAPI_PARAMS structure pointer [DHCP], dhcp.dhcpv6capi_params, dhcpv6csdk/DHCPV6CAPI_PARAMS, dhcpv6csdk/LPDHCPV6CAPI_PARAMS, dhcpv6csdk/PDHCPV6CAPI_PARAMS'
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCPV6CAPI_PARAMS, *PDHCPV6CAPI_PARAMS, *LPDHCPV6CAPI_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6CAPI_PARAMS
 - dhcpv6csdk/_DHCPV6CAPI_PARAMS
 - PDHCPV6CAPI_PARAMS
 - dhcpv6csdk/PDHCPV6CAPI_PARAMS
 - DHCPV6CAPI_PARAMS
 - dhcpv6csdk/DHCPV6CAPI_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpv6csdk.h
api_name:
 - DHCPV6CAPI_PARAMS
---

# DHCPV6CAPI_PARAMS structure


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

