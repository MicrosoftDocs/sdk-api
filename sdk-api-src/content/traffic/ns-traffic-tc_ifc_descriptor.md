---
UID: NS:traffic._TC_IFC_DESCRIPTOR
title: TC_IFC_DESCRIPTOR (traffic.h)
description: The TC_IFC_DESCRIPTOR structure is an interface identifier used to enumerate interfaces.
helpviewer_keywords: ["*PTC_IFC_DESCRIPTOR","PTC_IFC_DESCRIPTOR","PTC_IFC_DESCRIPTOR structure pointer [QOS]","TC_IFC_DESCRIPTOR","TC_IFC_DESCRIPTOR structure [QOS]","_gqos_tc_ifc_descriptor","qos.tc_ifc_descriptor","traffic/PTC_IFC_DESCRIPTOR","traffic/TC_IFC_DESCRIPTOR"]
old-location: qos\tc_ifc_descriptor.htm
tech.root: QOS
ms.assetid: 0ab0a17e-4055-43ee-81fd-c23fcecb8cb6
ms.date: 12/05/2018
ms.keywords: '*PTC_IFC_DESCRIPTOR, PTC_IFC_DESCRIPTOR, PTC_IFC_DESCRIPTOR structure pointer [QOS], TC_IFC_DESCRIPTOR, TC_IFC_DESCRIPTOR structure [QOS], _gqos_tc_ifc_descriptor, qos.tc_ifc_descriptor, traffic/PTC_IFC_DESCRIPTOR, traffic/TC_IFC_DESCRIPTOR'
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TC_IFC_DESCRIPTOR, *PTC_IFC_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TC_IFC_DESCRIPTOR
 - traffic/_TC_IFC_DESCRIPTOR
 - PTC_IFC_DESCRIPTOR
 - traffic/PTC_IFC_DESCRIPTOR
 - TC_IFC_DESCRIPTOR
 - traffic/TC_IFC_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - TC_IFC_DESCRIPTOR
---

# TC_IFC_DESCRIPTOR structure


## -description

The 
<b>TC_IFC_DESCRIPTOR</b> structure is an interface identifier used to enumerate interfaces.

## -struct-fields

### -field Length

Number of bytes from the beginning of the 
<b>TC_IFC_DESCRIPTOR</b> to the next 
<b>TC_IFC_DESCRIPTOR</b>.

### -field pInterfaceName

Pointer to a zero-terminated Unicode string representing the name of the packet shaper interface. This name is used in subsequent TC API calls to reference the interface.

### -field pInterfaceID

Pointer to a zero-terminated Unicode string naming the DeviceName of the interface.

### -field AddressListDesc

Network address list descriptor.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>