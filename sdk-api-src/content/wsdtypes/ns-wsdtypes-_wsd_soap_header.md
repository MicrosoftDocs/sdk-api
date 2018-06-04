---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


