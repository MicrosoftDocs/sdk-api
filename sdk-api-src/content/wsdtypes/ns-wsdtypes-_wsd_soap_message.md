---
UID: NS:wsdtypes._WSD_SOAP_MESSAGE
title: "_WSD_SOAP_MESSAGE"
author: windows-sdk-content
description: The contents of a WSD SOAP message.
old-location: ncd\wsd_soap_message_struct.htm
old-project: WsdApi
ms.assetid: e5352a78-3ece-45d3-bf95-2d922065e3d5
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSD_SOAP_MESSAGE, WSD_SOAP_MESSAGE structure, _WSD_SOAP_MESSAGE, ncd.wsd_soap_message_struct, wsdtypes/WSD_SOAP_MESSAGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SOAP_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_SOAP_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_SOAP_MESSAGE structure


## -description


The contents of a WSD SOAP message. This structure is used for <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> messages, ProbeMatch messages, <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a>  messages, and ResolveMatch messages, among others. 


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/6a0f0fd3-486e-45b3-bac6-e241bce8e2dc">WSD_SOAP_HEADER</a> structure that specifies the header of the SOAP message.


### -field Body

The body of the SOAP message.


### -field BodyType

Reference to a <a href="https://msdn.microsoft.com/dc214dfb-1717-4f84-af4d-6eb8cf17522c">WSDXML_TYPE</a> structure that specifies the type of the SOAP message body.


## -see-also




<a href="https://msdn.microsoft.com/52282990-d993-4034-a791-2ee7c9c1663d">Discovery and Metadata Exchange Messages</a>
 

 

