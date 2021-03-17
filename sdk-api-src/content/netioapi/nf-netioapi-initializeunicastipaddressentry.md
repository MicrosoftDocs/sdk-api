---
UID: NF:netioapi.InitializeUnicastIpAddressEntry
title: InitializeUnicastIpAddressEntry function (netioapi.h)
description: Initializes a MIB_UNICASTIPADDRESS_ROW structure with default values for a unicast IP address entry on the local computer.
helpviewer_keywords: ["InitializeUnicastIpAddressEntry","InitializeUnicastIpAddressEntry function [IP Helper]","iphlp.initializeunicastipaddressentry","netioapi/InitializeUnicastIpAddressEntry"]
old-location: iphlp\initializeunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: 8cbdd972-060a-4e18-9490-450df21936ea
ms.date: 12/05/2018
ms.keywords: InitializeUnicastIpAddressEntry, InitializeUnicastIpAddressEntry function [IP Helper], iphlp.initializeunicastipaddressentry, netioapi/InitializeUnicastIpAddressEntry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeUnicastIpAddressEntry
 - netioapi/InitializeUnicastIpAddressEntry
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
 - InitializeUnicastIpAddressEntry
---

# InitializeUnicastIpAddressEntry function


## -description

The 
<b>InitializeUnicastIpAddressEntry</b> function  initializes a <b>MIB_UNICASTIPADDRESS_ROW</b> structure with default values for a unicast IP address entry on the local computer.

## -parameters

### -param Row [out]

On entry, a pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry for a unicast IP address entry. On return, the  <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to by this parameter is initialized with default values for a unicast IP address.

## -returns

This function does not return a value.

## -remarks

The <b>InitializeUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeUnicastIpAddressEntry</b> function must be used to initialize the members of a
    <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry with default values for a unicast IP address for later use with the <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a> function.  

On input, <b>InitializeUnicastIpAddressEntry</b> must be passed a new <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure to initialize. 

On output, the <b>PrefixOrigin</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by <i>Row</i> parameter the will be initialized to <b>IpPrefixOriginUnchanged</b>, the <b>SuffixOrigin</b> member will be initialized to <b>IpSuffixOriginUnchanged</b>, and the  <b>OnLinkPrefixLength</b> member will be initialized to an illegal value. In addition, the <b>PreferredLifetime</b> and <b>ValidLifetime</b> members are set to infinite, the <b>SkipAsSource</b> member is set to <b>FALSE</b>, and other fields are initialized to zero. 

After calling <b>InitializeUnicastIpAddressEntry</b>, an application can then change the
    members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> entry it wishes to modify, and then call the <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>  to add the new unicast IP address to the local computer.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteunicastipaddressentry">DeleteUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>