---
UID: NS:wsdtypes._WSD_URI_LIST
title: WSD_URI_LIST (wsdtypes.h)
description: Represents a node in a linked list of URIs.
helpviewer_keywords: ["WSD_URI_LIST","WSD_URI_LIST structure","ncd.wsd_uri_list_struct","wsdtypes/WSD_URI_LIST"]
old-location: ncd\wsd_uri_list_struct.htm
tech.root: ncd
ms.assetid: 86d77741-39c3-44bd-b072-d2d4eb99e488
ms.date: 12/05/2018
ms.keywords: WSD_URI_LIST, WSD_URI_LIST structure, ncd.wsd_uri_list_struct, wsdtypes/WSD_URI_LIST
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
targetos: Windows
req.typenames: WSD_URI_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_URI_LIST
 - wsdtypes/_WSD_URI_LIST
 - WSD_URI_LIST
 - wsdtypes/WSD_URI_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_URI_LIST
---

# WSD_URI_LIST structure


## -description

Represents a node in a linked list of URIs.

## -struct-fields

### -field Next

Reference to the next node in the single-linked list of <b>WSD_URI_LIST</b> structures.

### -field Element

The URI referenced by this node.

