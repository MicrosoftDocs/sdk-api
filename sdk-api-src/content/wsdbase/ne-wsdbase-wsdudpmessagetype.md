---
UID: NE:wsdbase._WSDUdpMessageType
title: WSDUdpMessageType (wsdbase.h)
author: windows-sdk-content
description: Identifies the type of UDP message.
old-location: ncd\wsdudpmessagetype.htm
tech.root: WsdApi
ms.assetid: 0af4fd37-b1a9-4916-986c-e071c060d020
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ONE_WAY, TWO_WAY, WSDUdpMessageType, WSDUdpMessageType enumeration, ncd.wsdudpmessagetype, wsdbase/ONE_WAY, wsdbase/TWO_WAY, wsdbase/WSDUdpMessageType
ms.topic: enum
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
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
 - Wsdbase.h
api_name:
 - WSDUdpMessageType
product: Windows
targetos: Windows
req.typenames: WSDUdpMessageType
req.redist: 
---

# WSDUdpMessageType enumeration


## -description


Identifies the type of UDP message.


## -enum-fields




### -field ONE_WAY

The message is a one-way UDP message without a corresponding response. Hello and Bye messages are one-way messages.


### -field TWO_WAY

The message is a two-way UDP message with a corresponding response. Probe and Resolve messages are two-way messages.

