---
UID: NS:wsdtypes._WSD_RESOLVE
title: WSD_RESOLVE (wsdtypes.h)
author: windows-sdk-content
description: Represents a Resolve message.
old-location: ncd\wsd_resolve_struct.htm
tech.root: WsdApi
ms.assetid: f969f249-6c1e-4c0c-8da6-ec7069b06e20
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_RESOLVE, WSD_RESOLVE structure, ncd.wsd_resolve_struct, wsdtypes/WSD_RESOLVE
ms.topic: struct
f1_keywords:
- wsdtypes/WSD_RESOLVE
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
- WSD_RESOLVE
product: Windows
targetos: Windows
req.typenames: WSD_RESOLVE
req.redist: 
ms.custom: 19H1
---

# WSD_RESOLVE structure


## -description


Represents a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve</a> message.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies the endpoint to match. 


### -field Any

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve Message</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_resolve_match">WSD_RESOLVE_MATCH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_resolve_matches">WSD_RESOLVE_MATCHES</a>
 

 

