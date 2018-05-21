---
UID: NS:iprtrmib._TCPIP_OWNER_MODULE_BASIC_INFO
title: "_TCPIP_OWNER_MODULE_BASIC_INFO"
author: windows-driver-content
description: Contains pointers to the module name and module path values associated with a TCP connection. The TCPIP_OWNER_MODULE_BASIC_INFO structure is returned by the GetOwnerModuleFromTcpEntry and GetOwnerModuleFromTcp6Entry functions.
old-location: iphlp\tcpip_owner_module_basic_info.htm
old-project: IpHlp
ms.assetid: cce3e0ff-31f2-454b-8aae-3b35f72f47ed
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PTCPIP_OWNER_MODULE_BASIC_INFO, PTCPIP_OWNER_MODULE_BASIC_INFO, PTCPIP_OWNER_MODULE_BASIC_INFO structure pointer [IP Helper], TCPIP_OWNER_MODULE_BASIC_INFO, TCPIP_OWNER_MODULE_BASIC_INFO structure [IP Helper], _TCPIP_OWNER_MODULE_BASIC_INFO, iphlp.tcpip_owner_module_basic_info, iphlpapi/PTCPIP_OWNER_MODULE_BASIC_INFO, iphlpapi/TCPIP_OWNER_MODULE_BASIC_INFO, iprtrmib/PTCPIP_OWNER_MODULE_BASIC_INFO, iprtrmib/TCPIP_OWNER_MODULE_BASIC_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: TCPIP_OWNER_MODULE_BASIC_INFO, *PTCPIP_OWNER_MODULE_BASIC_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iprtrmib.h
-	Iphlpapi.h
api_name:
-	TCPIP_OWNER_MODULE_BASIC_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _TCPIP_OWNER_MODULE_BASIC_INFO structure


## -description


The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure contains pointers to the module name and module path values associated with a TCP connection. The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is returned by the <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> and <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> functions.


## -struct-fields




### -field pModuleName

A pointer to the name of the module. This field should be a <b>NULL</b> pointer when passed to <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> or <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> function.


### -field pModulePath

A pointer to the full path of the module, including the module name. This field should be a <b>NULL</b> pointer when passed to <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> or <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> function.


## -remarks



If the module owner is the system kernel, the <b>lpModuleName</b> and <b>lpModulePath</b> members point to a wide character string that contains "System".

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is defined in the <i>Iprtrmib.h</i> header file. 



