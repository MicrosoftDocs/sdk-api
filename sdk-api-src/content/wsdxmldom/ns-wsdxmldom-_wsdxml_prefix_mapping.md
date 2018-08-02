---
UID: NS:wsdxmldom._WSDXML_PREFIX_MAPPING
title: "_WSDXML_PREFIX_MAPPING"
author: windows-sdk-content
description: Describes an XML namespace prefix.
old-location: ncd\wsdxml_prefix_mapping_struct.htm
old-project: WsdApi
ms.assetid: d49a155a-a71b-4038-86a8-eb398db64e72
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSDXML_PREFIX_MAPPING, WSDXML_PREFIX_MAPPING structure, _WSDXML_PREFIX_MAPPING, ncd.wsdxml_prefix_mapping_struct, wsdxmldom/WSDXML_PREFIX_MAPPING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdxmldom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSDXML_PREFIX_MAPPING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXmldom.h
api_name:
 - WSDXML_PREFIX_MAPPING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSDXML_PREFIX_MAPPING structure


## -description


Describes an XML namespace prefix.


## -struct-fields




### -field Refs

The number of references to the mapping. When the value reaches zero, the mapping is deleted.


### -field Next

Reference to the next node in a linked list of <b>WSDXML_PREFIX_MAPPING</b> structures.


### -field Space

Reference to a <a href="https://msdn.microsoft.com/dcf27f38-e628-4b0c-859c-ad12d3ed0924">WSDXML_NAMESPACE</a> structure.


### -field Prefix

The text of the XML prefix.

