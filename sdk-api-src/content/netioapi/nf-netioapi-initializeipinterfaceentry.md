---
UID: NF:netioapi.InitializeIpInterfaceEntry
title: InitializeIpInterfaceEntry function (netioapi.h)
description: Initializes the members of an MIB_IPINTERFACE_ROW entry with default values.
helpviewer_keywords: ["InitializeIpInterfaceEntry","InitializeIpInterfaceEntry function [IP Helper]","iphlp.initializeipinterfaceentry","netioapi/InitializeIpInterfaceEntry"]
old-location: iphlp\initializeipinterfaceentry.htm
tech.root: IpHlp
ms.assetid: 5e7aed65-63e1-4e7b-bccf-9a2485212432
ms.date: 12/05/2018
ms.keywords: InitializeIpInterfaceEntry, InitializeIpInterfaceEntry function [IP Helper], iphlp.initializeipinterfaceentry, netioapi/InitializeIpInterfaceEntry
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
 - InitializeIpInterfaceEntry
 - netioapi/InitializeIpInterfaceEntry
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
 - InitializeIpInterfaceEntry
---

# InitializeIpInterfaceEntry function


## -description

The 
<b>InitializeIpInterfaceEntry</b> function  initializes the members of
    an <b>MIB_IPINTERFACE_ROW</b> entry with default values.

## -parameters

### -param Row [in, out]

A pointer to a 
<b>MIB_IPINTERFACE_ROW</b> structure to initialize. On successful return, the fields in this parameter are initialized with default information for an interface on the local computer.

## -returns

This function does not return a value.

## -remarks

The <b>InitializeIpInterfaceEntry</b> function is defined on Windows Vista and later. 

On output, the <b>Family</b> member in the <b>MIB_IPINTERFACE_ROW</b> structure pointed to by the <i>Row</i> parameter will be initialized to either <b>AF_UNSPEC</b>, the <b>InterfaceLuid</b> member in the <b>MIB_IPINTERFACE_ROW</b> structure will be initialized to an unspecified value, and other fields are initialized to zero. 

The <b>InitializeIpInterfaceEntry</b> function must be used to initialize the fields of a
    <b>MIB_IPINTERFACE_ROW</b> structure entry with default values.  An application can then change the
    fields in the <b>MIB_IPINTERFACE_ROW</b> entry it wishes to modify, and then call the <a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a> function.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfacetable">GetIpInterfaceTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<b>MIB_IPINTERFACE_ROW</b>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a>