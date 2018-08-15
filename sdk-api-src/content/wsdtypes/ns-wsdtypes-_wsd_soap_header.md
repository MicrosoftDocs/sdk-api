---
UID: NS:wsdtypes._WSD_SOAP_HEADER
title: "_WSD_SOAP_HEADER"
author: windows-sdk-content
description: Provides SOAP header data for the WSD_SOAP_MESSAGE structure.
old-location: ncd\wsd_soap_header_struct.htm
old-project: wsdapi
ms.assetid: 6a0f0fd3-486e-45b3-bac6-e241bce8e2dc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_SOAP_HEADER, WSD_SOAP_HEADER structure, _WSD_SOAP_HEADER, ncd.wsd_soap_header_struct, wsdtypes/WSD_SOAP_HEADER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.redist: 
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
tech.root: 
req.typenames: WSD_SOAP_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_SOAP_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_SOAP_HEADER structure


## -description


Provides SOAP header data for the <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure.




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

In request messages, a reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies to the endpoint to which responses should be sent.


### -field From

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint from which the SOAP message was sent.


### -field FaultTo

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies to the endpoint to which fault messages should be sent.


### -field AppSequence

In discovery messages, a reference to a <a href="https://msdn.microsoft.com/e9aa8e2f-0162-4f2e-ad70-54b6352105f9">WSD_APP_SEQUENCE</a> structure that helps the recipient determine the order in which messages were issued by the sender.


### -field AnyHeaders

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies additional headers not encoded by the other members. 


