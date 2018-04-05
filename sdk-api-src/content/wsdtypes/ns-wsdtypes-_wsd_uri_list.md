---
UID: NS:wsdtypes._WSD_URI_LIST
title: "_WSD_URI_LIST"
author: windows-driver-content
description: Represents a node in a linked list of URIs.
old-location: ncd\wsd_uri_list_struct.htm
old-project: WsdApi
ms.assetid: 86d77741-39c3-44bd-b072-d2d4eb99e488
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_URI_LIST, WSD_URI_LIST structure, _WSD_URI_LIST, ncd.wsd_uri_list_struct, wsdtypes/WSD_URI_LIST
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_URI_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_URI_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_URI_LIST structure


## -description


Represents a node in a linked list of URIs.


## -struct-fields




### -field Next

Reference to the next node in the single-linked list of <b>WSD_URI_LIST</b> structures.


### -field Element

The URI referenced by this node.

