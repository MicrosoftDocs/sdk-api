---
UID: NS:wsdtypes._WSD_REFERENCE_PROPERTIES
title: WSD_REFERENCE_PROPERTIES (wsdtypes.h)
description: Specifies additional data used to uniquely identify an endpoint.
helpviewer_keywords: ["WSD_REFERENCE_PROPERTIES","WSD_REFERENCE_PROPERTIES structure","ncd.wsd_reference_properties_struct","wsdtypes/WSD_REFERENCE_PROPERTIES"]
old-location: ncd\wsd_reference_properties_struct.htm
tech.root: ncd
ms.assetid: 7573683c-e02c-488d-be2f-f549113e78d9
ms.date: 12/05/2018
ms.keywords: WSD_REFERENCE_PROPERTIES, WSD_REFERENCE_PROPERTIES structure, ncd.wsd_reference_properties_struct, wsdtypes/WSD_REFERENCE_PROPERTIES
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
req.typenames: WSD_REFERENCE_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_REFERENCE_PROPERTIES
 - wsdtypes/_WSD_REFERENCE_PROPERTIES
 - WSD_REFERENCE_PROPERTIES
 - wsdtypes/WSD_REFERENCE_PROPERTIES
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
 - WSD_REFERENCE_PROPERTIES
---

# WSD_REFERENCE_PROPERTIES structure


## -description

Specifies additional data used to uniquely identify an endpoint.

## -struct-fields

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a>