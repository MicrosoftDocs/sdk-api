---
UID: NS:wsdtypes._WSD_SOAP_HEADER
title: WSD_SOAP_HEADER (wsdtypes.h)
description: Provides SOAP header data for the WSD_SOAP_MESSAGE structure.
helpviewer_keywords: ["WSD_SOAP_HEADER","WSD_SOAP_HEADER structure","ncd.wsd_soap_header_struct","wsdtypes/WSD_SOAP_HEADER"]
old-location: ncd\wsd_soap_header_struct.htm
tech.root: ncd
ms.assetid: 6a0f0fd3-486e-45b3-bac6-e241bce8e2dc
ms.date: 12/05/2018
ms.keywords: WSD_SOAP_HEADER, WSD_SOAP_HEADER structure, ncd.wsd_soap_header_struct, wsdtypes/WSD_SOAP_HEADER
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
req.typenames: WSD_SOAP_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SOAP_HEADER
 - wsdtypes/_WSD_SOAP_HEADER
 - WSD_SOAP_HEADER
 - wsdtypes/WSD_SOAP_HEADER
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
 - WSD_SOAP_HEADER
---

# WSD_SOAP_HEADER structure


## -description

Provides SOAP header data for the <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_message">WSD_SOAP_MESSAGE</a> structure.

## -struct-fields

### -field To

The URI to which the SOAP message is addressed.

### -field Action

The action encoded by the SOAP message.

### -field MessageID

An identifier that distinguishes the message from others from the same sender.

### -field RelatesTo

In response messages, specifies the message ID of the matching request message.

### -field ReplyTo

In request messages, a reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies to the endpoint to which responses should be sent.

### -field From

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint from which the SOAP message was sent.

### -field FaultTo

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies to the endpoint to which fault messages should be sent.

### -field AppSequence

In discovery messages, a reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_app_sequence">WSD_APP_SEQUENCE</a> structure that helps the recipient determine the order in which messages were issued by the sender.

### -field AnyHeaders

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies additional headers not encoded by the other members.