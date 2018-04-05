---
UID: NS:ks.KSTOPOLOGY_CONNECTION
title: KSTOPOLOGY_CONNECTION
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 2 or later. The KSTOPOLOGY_CONNECTION structure describes a node connection within a kernel-streaming (KS) filter. A node can be connected to another node within the filter, or to a pin on the filter.
old-location: dshow\kstopology_connection.htm
old-project: DirectShow
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PKSTOPOLOGY_CONNECTION, KSTOPOLOGY_CONNECTION, KSTOPOLOGY_CONNECTION structure [DirectShow], KSTOPOLOGY_CONNECTIONStructure, PKSTOPOLOGY_CONNECTION, PKSTOPOLOGY_CONNECTION structure pointer [DirectShow], dshow.kstopology_connection, ks/KSTOPOLOGY_CONNECTION, ks/PKSTOPOLOGY_CONNECTION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: 
req.target-type: Windows
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
req.typenames: KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ks.h
api_name:
-	KSTOPOLOGY_CONNECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# KSTOPOLOGY_CONNECTION structure


## -description



This topic applies to Windows XP Service Pack 2 or later.
          

The <b>KSTOPOLOGY_CONNECTION</b> structure describes a node connection within a kernel-streaming (KS) filter. A node can be connected to another node within the filter, or to a pin on the filter.




## -struct-fields




### -field FromNode

Index of the upstream node in the connection. If the upstream connection is a pin, rather than a node, the value is KSFILTER_NODE.


### -field FromNodePin

If the value of the <b>FromNode</b> field is KSFILTER_NODE, this field specifies the index of the upstream pin. Otherwise, this field is ignored.


### -field ToNode

Index of the downstream node in the connection. If the downstream connection is a pin, rather than a node, the value is KSFILTER_NODE.


### -field ToNodePin

If the value of the <b>ToNode</b> field is KSFILTER_NODE, this field specifies the index of the downstream pin. Otherwise, this field is ignored.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/ef062e0f-0866-48ca-bd27-26000cd4983a">IKsTopologyInfo::get_ConnectionInfo</a>
 

 

