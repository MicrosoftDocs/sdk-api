---
UID: NS:ntddndis._NDIS_OBJECT_HEADER
title: "_NDIS_OBJECT_HEADER"
author: windows-driver-content
description: Packages the object type, version, and size information that is required in many NDIS 6.0 structures.
old-location: nwifi\ndis_object_header.htm
old-project: NativeWiFi
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PNDIS_OBJECT_HEADER, NDIS_OBJECT_HEADER, NDIS_OBJECT_HEADER structure [NativeWIFI], PNDIS_OBJECT_HEADER, PNDIS_OBJECT_HEADER structure pointer [NativeWIFI], _NDIS_OBJECT_HEADER, ntddndis/NDIS_OBJECT_HEADER, ntddndis/PNDIS_OBJECT_HEADER, nwifi.ndis_object_header"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddndis.h
req.include-header: Windot11.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
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
req.typenames: NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddndis.h
api_name:
-	NDIS_OBJECT_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _NDIS_OBJECT_HEADER structure


## -description


The <b>NDIS_OBJECT_HEADER</b> structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.


## -struct-fields




### -field Type

Specifies the type of NDIS object that a structure describes.


### -field Revision

Specifies the revision number of this structure.


### -field Size

Specifies the total size, in bytes, of the NDIS structure that contains the <b>NDIS_OBJECT_HEADER</b>.  This size includes the size of the <b>NDIS_OBJECT_HEADER</b> member and all other members of the structure.


## -see-also




<a href="https://msdn.microsoft.com/22907f94-1ae8-4938-a816-b406656256c0">DOT11_BSSID_LIST</a>
 

 

