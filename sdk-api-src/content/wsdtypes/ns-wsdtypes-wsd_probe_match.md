---
UID: NS:wsdtypes._WSD_PROBE_MATCH
title: WSD_PROBE_MATCH (wsdtypes.h)
description: Represents a ProbeMatch message.
helpviewer_keywords: ["WSD_PROBE_MATCH","WSD_PROBE_MATCH structure","ncd.wsd_probe_match_struct","wsdtypes/WSD_PROBE_MATCH"]
old-location: ncd\wsd_probe_match_struct.htm
tech.root: ncd
ms.assetid: a30b11c8-df26-495d-87c3-aa67e400ec28
ms.date: 12/05/2018
ms.keywords: WSD_PROBE_MATCH, WSD_PROBE_MATCH structure, ncd.wsd_probe_match_struct, wsdtypes/WSD_PROBE_MATCH
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
req.typenames: WSD_PROBE_MATCH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PROBE_MATCH
 - wsdtypes/_WSD_PROBE_MATCH
 - WSD_PROBE_MATCH
 - wsdtypes/WSD_PROBE_MATCH
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
 - WSD_PROBE_MATCH
---

# WSD_PROBE_MATCH structure


## -description

Represents a ProbeMatch message.

## -struct-fields

### -field EndpointReference

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure that specifies the matching endpoint.

### -field Types

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.

### -field Scopes

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_scopes">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.

### -field XAddrs

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that contains a list of WS-Discovery XAddrs.

### -field MetadataVersion

The metadata version of this message.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/probe-message">Probe Message</a>



<a href="/windows/desktop/WsdApi/probematches-message">ProbeMatches Message</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe">WSD_PROBE</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_matches">WSD_PROBE_MATCHES</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match_list">WSD_PROBE_MATCH_LIST</a>