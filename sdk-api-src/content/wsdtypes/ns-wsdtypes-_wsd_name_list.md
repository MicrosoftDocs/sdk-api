---
UID: NS:wsdtypes._WSD_NAME_LIST
title: "_WSD_NAME_LIST"
author: windows-driver-content
description: Represents a node in a single-linked list of XML name structures.
old-location: ncd\wsd_name_list_struct.htm
old-project: WsdApi
ms.assetid: f573365d-100f-4df9-b1af-a484680436eb
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_NAME_LIST, WSD_NAME_LIST structure, _WSD_NAME_LIST, ncd.wsd_name_list_struct, wsdtypes/WSD_NAME_LIST
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
req.typenames: WSD_NAME_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_NAME_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_NAME_LIST structure


## -description


Represents a node in a single-linked list of XML name structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_NAME_LIST</b> structures.


### -field Element

The XML qualified name data referenced by this node.

