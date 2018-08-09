---
UID: NS:wsdtypes._WSD_METADATA_SECTION_LIST
title: "_WSD_METADATA_SECTION_LIST"
author: windows-sdk-content
description: Represents a node in a single-linked list of metadata sections.
old-location: ncd\wsd_metadata_section_list_struct.htm
old-project: wsdapi
ms.assetid: e5c6373a-f365-499d-a971-472ffa557a41
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_METADATA_SECTION_LIST, WSD_METADATA_SECTION_LIST structure, _WSD_METADATA_SECTION_LIST, ncd.wsd_metadata_section_list_struct, wsdtypes/WSD_METADATA_SECTION_LIST
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_METADATA_SECTION_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_METADATA_SECTION_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_METADATA_SECTION_LIST structure


## -description


Represents a node in a single-linked list of metadata sections.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_METADATA_SECTION_LIST</b> structures.


### -field Element

The metadata section referenced by this node.

