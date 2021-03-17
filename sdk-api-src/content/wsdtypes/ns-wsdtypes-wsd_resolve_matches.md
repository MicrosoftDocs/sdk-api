---
UID: NS:wsdtypes._WSD_RESOLVE_MATCHES
title: WSD_RESOLVE_MATCHES (wsdtypes.h)
description: Represents a ResolveMatches message.
helpviewer_keywords: ["WSD_RESOLVE_MATCHES","WSD_RESOLVE_MATCHES structure","ncd.wsd_resolve_matches","wsdtypes/WSD_RESOLVE_MATCHES"]
old-location: ncd\wsd_resolve_matches.htm
tech.root: ncd
ms.assetid: a6094069-af17-4921-b2c3-4ec89cbbb6f6
ms.date: 12/05/2018
ms.keywords: WSD_RESOLVE_MATCHES, WSD_RESOLVE_MATCHES structure, ncd.wsd_resolve_matches, wsdtypes/WSD_RESOLVE_MATCHES
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
req.typenames: WSD_RESOLVE_MATCHES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_RESOLVE_MATCHES
 - wsdtypes/_WSD_RESOLVE_MATCHES
 - WSD_RESOLVE_MATCHES
 - wsdtypes/WSD_RESOLVE_MATCHES
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
 - WSD_RESOLVE_MATCHES
---

# WSD_RESOLVE_MATCHES structure


## -description

Represents a <a href="/windows/desktop/WsdApi/resolve-message">ResolveMatches</a> message.

## -struct-fields

### -field ResolveMatch

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_resolve_match">WSD_RESOLVE_MATCH</a> structure that contains a child ResolveMatch message.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/resolve-message">ResolveMatches Message</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_resolve">WSD_RESOLVE</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_resolve_match">WSD_RESOLVE_MATCH</a>