---
UID: NS:wsdtypes._WSD_SOAP_MESSAGE
title: WSD_SOAP_MESSAGE (wsdtypes.h)
description: The contents of a WSD SOAP message.
old-location: ncd\wsd_soap_message_struct.htm
tech.root: WsdApi
ms.assetid: e5352a78-3ece-45d3-bf95-2d922065e3d5
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_MESSAGE, WSD_SOAP_MESSAGE structure, ncd.wsd_soap_message_struct, wsdtypes/WSD_SOAP_MESSAGE
ms.topic: struct
f1_keywords:
- wsdtypes/WSD_SOAP_MESSAGE
dev_langs:
- c++
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
- WSD_SOAP_MESSAGE
targetos: Windows
req.typenames: WSD_SOAP_MESSAGE
req.redist: 
ms.custom: 19H1
---

# WSD_SOAP_MESSAGE structure


## -description


The contents of a WSD SOAP message. This structure is used for <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probe-message">Probe</a> messages, ProbeMatch messages, <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve</a>  messages, and ResolveMatch messages, among others. 


## -struct-fields




### -field Header

A <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_header">WSD_SOAP_HEADER</a> structure that specifies the header of the SOAP message.


### -field Body

The body of the SOAP message.


### -field BodyType

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_type">WSDXML_TYPE</a> structure that specifies the type of the SOAP message body.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/discovery-and-metadata-exchange-message-patterns">Discovery and Metadata Exchange Messages</a>
 

 

