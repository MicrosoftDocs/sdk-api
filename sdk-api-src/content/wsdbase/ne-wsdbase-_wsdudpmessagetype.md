---
UID: NE:wsdbase._WSDUdpMessageType
title: "_WSDUdpMessageType"
author: windows-sdk-content
description: Identifies the type of UDP message.
old-location: ncd\wsdudpmessagetype.htm
old-project: wsdapi
ms.assetid: 0af4fd37-b1a9-4916-986c-e071c060d020
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ONE_WAY, TWO_WAY, WSDUdpMessageType, WSDUdpMessageType enumeration, _WSDUdpMessageType, ncd.wsdudpmessagetype, wsdbase/ONE_WAY, wsdbase/TWO_WAY, wsdbase/WSDUdpMessageType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSDUdpMessageType
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
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSDUdpMessageType enumeration


## -description


Identifies the type of UDP message.


## -enum-fields




### -field ONE_WAY

The message is a one-way UDP message without a corresponding response. Hello and Bye messages are one-way messages.


### -field TWO_WAY

The message is a two-way UDP message with a corresponding response. Probe and Resolve messages are two-way messages.

