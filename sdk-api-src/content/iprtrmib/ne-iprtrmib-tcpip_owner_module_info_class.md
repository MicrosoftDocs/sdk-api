---
UID: NE:iprtrmib._TCPIP_OWNER_MODULE_INFO_CLASS
title: TCPIP_OWNER_MODULE_INFO_CLASS (iprtrmib.h)
description: Defines the type of module information structure passed to calls of the GetOwnerModuleFromXXXEntry family.
helpviewer_keywords: ["*PTCPIP_OWNER_MODULE_INFO_CLASS","PTCPIP_OWNER_MODULE_INFO_CLASS","PTCPIP_OWNER_MODULE_INFO_CLASS enumeration pointer [IP Helper]","TCPIP_OWNER_MODULE_INFO_BASIC","TCPIP_OWNER_MODULE_INFO_CLASS","TCPIP_OWNER_MODULE_INFO_CLASS enumeration [IP Helper]","iphlp.tcpip_owner_module_info_class","iprtrmib/PTCPIP_OWNER_MODULE_INFO_CLASS","iprtrmib/TCPIP_OWNER_MODULE_INFO_BASIC","iprtrmib/TCPIP_OWNER_MODULE_INFO_CLASS"]
old-location: iphlp\tcpip_owner_module_info_class.htm
tech.root: IpHlp
ms.assetid: 8529dd62-8516-47d0-8118-95e6d33fc799
ms.date: 12/05/2018
ms.keywords: '*PTCPIP_OWNER_MODULE_INFO_CLASS, PTCPIP_OWNER_MODULE_INFO_CLASS, PTCPIP_OWNER_MODULE_INFO_CLASS enumeration pointer [IP Helper], TCPIP_OWNER_MODULE_INFO_BASIC, TCPIP_OWNER_MODULE_INFO_CLASS, TCPIP_OWNER_MODULE_INFO_CLASS enumeration [IP Helper], iphlp.tcpip_owner_module_info_class, iprtrmib/PTCPIP_OWNER_MODULE_INFO_CLASS, iprtrmib/TCPIP_OWNER_MODULE_INFO_BASIC, iprtrmib/TCPIP_OWNER_MODULE_INFO_CLASS'
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
req.typenames: TCPIP_OWNER_MODULE_INFO_CLASS, *PTCPIP_OWNER_MODULE_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCPIP_OWNER_MODULE_INFO_CLASS
 - iprtrmib/_TCPIP_OWNER_MODULE_INFO_CLASS
 - PTCPIP_OWNER_MODULE_INFO_CLASS
 - iprtrmib/PTCPIP_OWNER_MODULE_INFO_CLASS
 - TCPIP_OWNER_MODULE_INFO_CLASS
 - iprtrmib/TCPIP_OWNER_MODULE_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - TCPIP_OWNER_MODULE_INFO_CLASS
---

# TCPIP_OWNER_MODULE_INFO_CLASS enumeration


## -description

The <b>TCPIP_OWNER_MODULE_INFO_CLASS</b> enumeration defines the type of module information structure passed to calls of the <b>GetOwnerModuleFromXXXEntry</b> family.

## -enum-fields

### -field TCPIP_OWNER_MODULE_INFO_BASIC

A <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure is passed to the <b>GetOwnerModuleFromXXXEntry</b> function.