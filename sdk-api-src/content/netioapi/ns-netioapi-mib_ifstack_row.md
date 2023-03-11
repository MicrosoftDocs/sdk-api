---
UID: NS:netioapi._MIB_IFSTACK_ROW
title: MIB_IFSTACK_ROW (netioapi.h)
description: Represents the relationship between two network interfaces. (MIB_IFSTACK_ROW)
helpviewer_keywords: ["*PMIB_IFSTACK_ROW","MIB_IFSTACK_ROW","MIB_IFSTACK_ROW structure [MIB]","PMIB_IFSTACK_ROW","PMIB_IFSTACK_ROW structure pointer [MIB]","_MIB_IFSTACK_ROW","mib.mib_ifstack_row","netioapi/MIB_IFSTACK_ROW","netioapi/PMIB_IFSTACK_ROW"]
old-location: mib\mib_ifstack_row.htm
tech.root: MIB
ms.assetid: f86dfb52-98e8-4725-990c-5de788bebef1
ms.date: 12/05/2018
ms.keywords: '*PMIB_IFSTACK_ROW, MIB_IFSTACK_ROW, MIB_IFSTACK_ROW structure [MIB], PMIB_IFSTACK_ROW, PMIB_IFSTACK_ROW structure pointer [MIB], _MIB_IFSTACK_ROW, mib.mib_ifstack_row, netioapi/MIB_IFSTACK_ROW, netioapi/PMIB_IFSTACK_ROW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_IFSTACK_ROW, *PMIB_IFSTACK_ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IFSTACK_ROW
 - netioapi/_MIB_IFSTACK_ROW
 - PMIB_IFSTACK_ROW
 - netioapi/PMIB_IFSTACK_ROW
 - MIB_IFSTACK_ROW
 - netioapi/MIB_IFSTACK_ROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_IFSTACK_ROW
---

# MIB_IFSTACK_ROW structure


## -description

The 
<b>MIB_IFSTACK_ROW</b> structure represents the relationship between two network interfaces.

## -struct-fields

### -field HigherLayerInterfaceIndex

The network interface index for the interface that is higher in the interface stack table.

### -field LowerLayerInterfaceIndex

The network interface index for the interface that is lower in the interface stack table.

## -remarks

The <b>MIB_IFSTACK_ROW</b> structure is defined in Windows Vista and later. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member.

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getifstacktable">GetIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getinvertedifstacktable">GetInvertedIfStackTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ifstack_table">MIB_IFSTACK_TABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a>
