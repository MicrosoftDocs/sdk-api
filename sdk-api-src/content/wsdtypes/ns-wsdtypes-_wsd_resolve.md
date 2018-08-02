---
UID: NS:wsdtypes._WSD_RESOLVE
title: "_WSD_RESOLVE"
author: windows-sdk-content
description: Represents a Resolve message.
old-location: ncd\wsd_resolve_struct.htm
old-project: WsdApi
ms.assetid: f969f249-6c1e-4c0c-8da6-ec7069b06e20
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSD_RESOLVE, WSD_RESOLVE structure, _WSD_RESOLVE, ncd.wsd_resolve_struct, wsdtypes/WSD_RESOLVE
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_RESOLVE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_RESOLVE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_RESOLVE structure


## -description


Represents a <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a> message.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint to match. 


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve Message</a>



<a href="https://msdn.microsoft.com/eabcc3af-282c-4299-8061-6cddf14eca6b">WSD_RESOLVE_MATCH</a>



<a href="https://msdn.microsoft.com/a6094069-af17-4921-b2c3-4ec89cbbb6f6">WSD_RESOLVE_MATCHES</a>
 

 

