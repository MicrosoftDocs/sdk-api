---
UID: NS:iprtrmib._TCPIP_OWNER_MODULE_BASIC_INFO
title: TCPIP_OWNER_MODULE_BASIC_INFO (iprtrmib.h)
description: Contains pointers to the module name and module path values associated with a TCP connection. The TCPIP_OWNER_MODULE_BASIC_INFO structure is returned by the GetOwnerModuleFromTcpEntry and GetOwnerModuleFromTcp6Entry functions.
helpviewer_keywords: ["*PTCPIP_OWNER_MODULE_BASIC_INFO","PTCPIP_OWNER_MODULE_BASIC_INFO","PTCPIP_OWNER_MODULE_BASIC_INFO structure pointer [IP Helper]","TCPIP_OWNER_MODULE_BASIC_INFO","TCPIP_OWNER_MODULE_BASIC_INFO structure [IP Helper]","iphlp.tcpip_owner_module_basic_info","iphlpapi/PTCPIP_OWNER_MODULE_BASIC_INFO","iphlpapi/TCPIP_OWNER_MODULE_BASIC_INFO","iprtrmib/PTCPIP_OWNER_MODULE_BASIC_INFO","iprtrmib/TCPIP_OWNER_MODULE_BASIC_INFO"]
old-location: iphlp\tcpip_owner_module_basic_info.htm
tech.root: IpHlp
ms.assetid: cce3e0ff-31f2-454b-8aae-3b35f72f47ed
ms.date: 12/05/2018
ms.keywords: '*PTCPIP_OWNER_MODULE_BASIC_INFO, PTCPIP_OWNER_MODULE_BASIC_INFO, PTCPIP_OWNER_MODULE_BASIC_INFO structure pointer [IP Helper], TCPIP_OWNER_MODULE_BASIC_INFO, TCPIP_OWNER_MODULE_BASIC_INFO structure [IP Helper], iphlp.tcpip_owner_module_basic_info, iphlpapi/PTCPIP_OWNER_MODULE_BASIC_INFO, iphlpapi/TCPIP_OWNER_MODULE_BASIC_INFO, iprtrmib/PTCPIP_OWNER_MODULE_BASIC_INFO, iprtrmib/TCPIP_OWNER_MODULE_BASIC_INFO'
req.header: iprtrmib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: TCPIP_OWNER_MODULE_BASIC_INFO, *PTCPIP_OWNER_MODULE_BASIC_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCPIP_OWNER_MODULE_BASIC_INFO
 - iprtrmib/_TCPIP_OWNER_MODULE_BASIC_INFO
 - PTCPIP_OWNER_MODULE_BASIC_INFO
 - iprtrmib/PTCPIP_OWNER_MODULE_BASIC_INFO
 - TCPIP_OWNER_MODULE_BASIC_INFO
 - iprtrmib/TCPIP_OWNER_MODULE_BASIC_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
 - Iphlpapi.h
api_name:
 - TCPIP_OWNER_MODULE_BASIC_INFO
---

# TCPIP_OWNER_MODULE_BASIC_INFO structure


## -description

The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure contains pointers to the module name and module path values associated with a TCP connection. The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcpentry">GetOwnerModuleFromTcpEntry</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry">GetOwnerModuleFromTcp6Entry</a> functions.

## -struct-fields

### -field pModuleName

A pointer to the name of the module. This field should be a <b>NULL</b> pointer when passed to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcpentry">GetOwnerModuleFromTcpEntry</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry">GetOwnerModuleFromTcp6Entry</a> function.

### -field pModulePath

A pointer to the full path of the module, including the module name. This field should be a <b>NULL</b> pointer when passed to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcpentry">GetOwnerModuleFromTcpEntry</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry">GetOwnerModuleFromTcp6Entry</a> function.

## -remarks

If the module owner is the system kernel, the <b>lpModuleName</b> and <b>lpModulePath</b> members point to a wide character string that contains "System".

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is defined in the <i>Iprtrmib.h</i> header file.