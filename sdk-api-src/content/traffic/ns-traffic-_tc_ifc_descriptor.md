---
UID: NS:traffic._TC_IFC_DESCRIPTOR
title: "_TC_IFC_DESCRIPTOR"
author: windows-driver-content
description: The TC_IFC_DESCRIPTOR structure is an interface identifier used to enumerate interfaces.
old-location: qos\tc_ifc_descriptor.htm
old-project: QOS
ms.assetid: 0ab0a17e-4055-43ee-81fd-c23fcecb8cb6
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PTC_IFC_DESCRIPTOR, PTC_IFC_DESCRIPTOR, PTC_IFC_DESCRIPTOR structure pointer [QOS], TC_IFC_DESCRIPTOR, TC_IFC_DESCRIPTOR structure [QOS], _TC_IFC_DESCRIPTOR, _gqos_tc_ifc_descriptor, qos.tc_ifc_descriptor, traffic/PTC_IFC_DESCRIPTOR, traffic/TC_IFC_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: TC_IFC_DESCRIPTOR, *PTC_IFC_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Traffic.h
api_name:
-	TC_IFC_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TC_IFC_DESCRIPTOR structure


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




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

