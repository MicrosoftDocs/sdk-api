---
UID: NS:wsdtypes._WSD_NAME_LIST
title: WSD_NAME_LIST (wsdtypes.h)
author: windows-sdk-content
description: Represents a node in a single-linked list of XML name structures.
old-location: ncd\wsd_name_list_struct.htm
tech.root: WsdApi
ms.assetid: f573365d-100f-4df9-b1af-a484680436eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_NAME_LIST, WSD_NAME_LIST structure, ncd.wsd_name_list_struct, wsdtypes/WSD_NAME_LIST
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_NAME_LIST
product: Windows
targetos: Windows
req.typenames: WSD_NAME_LIST
req.redist: 
---

# WSD_NAME_LIST structure


## -description


Represents a node in a single-linked list of XML name structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_NAME_LIST</b> structures.


### -field Element

The XML qualified name data referenced by this node.

