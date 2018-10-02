---
UID: NS:wsdtypes._WSD_RELATIONSHIP_METADATA
title: "_WSD_RELATIONSHIP_METADATA"
author: windows-sdk-content
description: Provides metadata about the relationship between two or more services.
old-location: ncd\wsd_relationship_metadata.htm
tech.root: WsdApi
ms.assetid: 232ea033-f368-4a37-9bec-ba5dc0d9b60f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSD_RELATIONSHIP_METADATA, WSD_RELATIONSHIP_METADATA structure, _WSD_RELATIONSHIP_METADATA, ncd.wsd_relationship_metadata, wsdtypes/WSD_RELATIONSHIP_METADATA
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
 - WSD_RELATIONSHIP_METADATA
product: Windows
targetos: Windows
req.typenames: WSD_RELATIONSHIP_METADATA
req.redist: 
---

# _WSD_RELATIONSHIP_METADATA structure


## -description


Provides metadata about the relationship between two or more services.


## -struct-fields




### -field Type

A WS-Discovery Type.


### -field Data

Reference to a <a href="https://msdn.microsoft.com/da774582-3b27-470d-9b6a-ac2b106a47b9">WSD_HOST_METADATA</a> structure that contains metadata for all services hosted by a device.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

