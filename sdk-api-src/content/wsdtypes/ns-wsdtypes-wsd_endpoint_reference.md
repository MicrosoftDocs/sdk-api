---
UID: NS:wsdtypes._WSD_ENDPOINT_REFERENCE
title: WSD_ENDPOINT_REFERENCE (wsdtypes.h)
author: windows-sdk-content
description: Represents a WS-Addressing endpoint reference.
old-location: ncd\wsd_endpoint_reference_struct.htm
tech.root: WsdApi
ms.assetid: 97d6870e-3633-4bea-9a50-984e6b0ba3a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_ENDPOINT_REFERENCE, WSD_ENDPOINT_REFERENCE structure, ncd.wsd_endpoint_reference_struct, wsdtypes/WSD_ENDPOINT_REFERENCE
ms.topic: struct
f1_keywords: ["wsdtypes/WSD_ENDPOINT_REFERENCE"]
req.header: wsdtypes.h
req.include-header: 
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
 - Wsdtypes.h
api_name:
 - WSD_ENDPOINT_REFERENCE
product: Windows
targetos: Windows
req.typenames: WSD_ENDPOINT_REFERENCE
req.redist: 
ms.custom: 19H1
---

# WSD_ENDPOINT_REFERENCE structure


## -description


Represents a WS-Addressing endpoint reference.


## -struct-fields




### -field Address

The endpoint address.


### -field ReferenceProperties


<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-_wsd_reference_properties">WSD_REFERENCE_PROPERTIES</a> structure that specifies additional data used to uniquely identify the endpoint.


### -field ReferenceParameters


<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-_wsd_reference_parameters">WSD_REFERENCE_PARAMETERS</a> structure that specifies additional opaque data used by the endpoint.


### -field PortType

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-_wsdxml_name">WSDXML_NAME</a> structure that specifies the port type of the service at the referenced endpoint.


### -field ServiceName

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-_wsdxml_name">WSDXML_NAME</a> structure that specifies the service name of the service at the referenced endpoint.


### -field Any

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-_wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

