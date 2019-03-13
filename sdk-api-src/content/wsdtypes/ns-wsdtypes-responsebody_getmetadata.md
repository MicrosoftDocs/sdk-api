---
UID: NS:wsdtypes.__unnamed_struct_0
title: RESPONSEBODY_GetMetadata
author: windows-sdk-content
description: Represents a WS-MetadataExchange GetMetadata response message.
old-location: ncd\responsebody_getmetadata_struct.htm
tech.root: WsdApi
ms.assetid: 445513a8-5785-4822-bb2e-ec9b7665ac7a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RESPONSEBODY_GetMetadata, RESPONSEBODY_GetMetadata structure, ncd.responsebody_getmetadata_struct, wsdtypes/RESPONSEBODY_GetMetadata
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
 - RESPONSEBODY_GetMetadata
product: Windows
targetos: Windows
req.typenames: RESPONSEBODY_GetMetadata
req.redist: 
---

# RESPONSEBODY_GetMetadata structure


## -description


Represents a WS-MetadataExchange GetMetadata response message.


## -struct-fields




### -field Metadata

Reference to a <a href="https://msdn.microsoft.com/e5c6373a-f365-499d-a971-472ffa557a41">WSD_METADATA_SECTION_LIST</a> structure that contains a node in a single-linked list of metadata sections.

