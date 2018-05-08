---
UID: NS:wsdtypes._WSD_SERVICE_METADATA_LIST
title: "_WSD_SERVICE_METADATA_LIST"
author: windows-driver-content
description: Represents a node in a single-linked list of service metadata structures.
old-location: ncd\wsd_service_metadata_list_struct.htm
old-project: WsdApi
ms.assetid: f5975443-00e3-44f0-9a69-02460d4312c5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_SERVICE_METADATA_LIST, WSD_SERVICE_METADATA_LIST structure, _WSD_SERVICE_METADATA_LIST, ncd.wsd_service_metadata_list_struct, wsdtypes/WSD_SERVICE_METADATA_LIST
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_SERVICE_METADATA_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_SERVICE_METADATA_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_SERVICE_METADATA_LIST structure


## -description


Represents a node in a single-linked list of service metadata structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_SERVICE_METADATA_LIST</b> structures. 



### -field Element

Reference to a <a href="https://msdn.microsoft.com/1f80e36f-06ca-41fc-bbd7-b44823c75d4d">WSD_SERVICE_METADATA</a> structure that represents the service metadata referenced by this node.


## -see-also




<a href="https://msdn.microsoft.com/1f80e36f-06ca-41fc-bbd7-b44823c75d4d">WSD_SERVICE_METADATA</a>
 

 

