---
UID: NS:wsdtypes._WSD_ENDPOINT_REFERENCE_LIST
title: WSD_ENDPOINT_REFERENCE_LIST (wsdtypes.h)
author: windows-sdk-content
description: Represents a node in a single-linked list of WSD_ENDPOINT_REFERENCE structures.
old-location: ncd\wsd_endpoint_reference_list.htm
tech.root: WsdApi
ms.assetid: fc9fed5c-8a5b-4960-836b-e083154b7d90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_ENDPOINT_REFERENCE_LIST, WSD_ENDPOINT_REFERENCE_LIST structure, ncd.wsd_endpoint_reference_list, wsdtypes/WSD_ENDPOINT_REFERENCE_LIST
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
 - WSD_ENDPOINT_REFERENCE_LIST
product: Windows
targetos: Windows
req.typenames: WSD_ENDPOINT_REFERENCE_LIST
req.redist: 
---

# WSD_ENDPOINT_REFERENCE_LIST structure


## -description


Represents a node in a single-linked list of <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_ENDPOINT_REFERENCE_LIST</b> structures.


### -field Element

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that contains the endpoint referenced by this node.


## -see-also




<a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a>
 

 

