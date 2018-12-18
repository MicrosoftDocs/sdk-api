---
UID: NS:wsdtypes._WSD_HELLO
title: WSD_HELLO
author: windows-sdk-content
description: Represents a Hello message.
old-location: ncd\wsd_hello_struct.htm
tech.root: wsdapi
ms.assetid: 71fad98a-d115-4350-b3aa-3f3927b2c24d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSD_HELLO, WSD_HELLO structure, ncd.wsd_hello_struct, wsdtypes/WSD_HELLO
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
 - WSD_HELLO
product: Windows
targetos: Windows
req.typenames: WSD_HELLO
req.redist: 
---

# WSD_HELLO structure


## -description


Represents a <a href="https://msdn.microsoft.com/a7402e02-9bdc-49ec-ba93-8a32f55b9dd8">Hello</a> message.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint announcing the Hello message. 


### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field Scopes

Reference to a <a href="https://msdn.microsoft.com/3415fef0-dbf4-4ece-bad0-6cd6831404db">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.


### -field XAddrs

Reference to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that contains a list of WS-Discovery XAddrs.


### -field MetadataVersion

The metadata version of this message.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/a7402e02-9bdc-49ec-ba93-8a32f55b9dd8">Hello Message</a>
 

 

