---
UID: NS:wsdtypes._WSD_ENDPOINT_REFERENCE
title: WSD_ENDPOINT_REFERENCE
author: windows-sdk-content
description: Represents a WS-Addressing endpoint reference.
old-location: ncd\wsd_endpoint_reference_struct.htm
tech.root: wsdapi
ms.assetid: 97d6870e-3633-4bea-9a50-984e6b0ba3a1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSD_ENDPOINT_REFERENCE, WSD_ENDPOINT_REFERENCE structure, ncd.wsd_endpoint_reference_struct, wsdtypes/WSD_ENDPOINT_REFERENCE
ms.topic: struct
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
---

# WSD_ENDPOINT_REFERENCE structure


## -description


Represents a WS-Addressing endpoint reference.


## -struct-fields




### -field Address

The endpoint address.


### -field ReferenceProperties


<a href="https://msdn.microsoft.com/7573683c-e02c-488d-be2f-f549113e78d9">WSD_REFERENCE_PROPERTIES</a> structure that specifies additional data used to uniquely identify the endpoint.


### -field ReferenceParameters


<a href="https://msdn.microsoft.com/add8bda6-b5b1-4026-9900-829ece926670">WSD_REFERENCE_PARAMETERS</a> structure that specifies additional opaque data used by the endpoint.


### -field PortType

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies the port type of the service at the referenced endpoint.


### -field ServiceName

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies the service name of the service at the referenced endpoint.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

