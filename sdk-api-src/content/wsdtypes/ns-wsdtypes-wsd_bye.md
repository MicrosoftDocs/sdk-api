---
UID: NS:wsdtypes._WSD_BYE
title: WSD_BYE (wsdtypes.h)
description: Represents a Bye message.
helpviewer_keywords: ["WSD_BYE","WSD_BYE structure","ncd.wsd_bye_struct","wsdtypes/WSD_BYE"]
old-location: ncd\wsd_bye_struct.htm
tech.root: ncd
ms.assetid: b0eb67e1-1408-45ab-b7a7-ecde6619a277
ms.date: 12/05/2018
ms.keywords: WSD_BYE, WSD_BYE structure, ncd.wsd_bye_struct, wsdtypes/WSD_BYE
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
req.typenames: WSD_BYE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_BYE
 - wsdtypes/_WSD_BYE
 - WSD_BYE
 - wsdtypes/WSD_BYE
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
 - WSD_BYE
---

# WSD_BYE structure


## -description

Represents a <a href="/windows/desktop/WsdApi/bye-message">Bye</a> message.

## -struct-fields

### -field EndpointReference

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies either the sending or receiving endpoint of the Bye message.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/bye-message">Bye Message</a>