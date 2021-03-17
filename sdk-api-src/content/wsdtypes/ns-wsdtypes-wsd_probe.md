---
UID: NS:wsdtypes._WSD_PROBE
title: WSD_PROBE (wsdtypes.h)
description: Represents a Probe message.
helpviewer_keywords: ["WSD_PROBE","WSD_PROBE structure","ncd.wsd_probe_struct","wsdtypes/WSD_PROBE"]
old-location: ncd\wsd_probe_struct.htm
tech.root: ncd
ms.assetid: f84f7e77-ffe2-41af-a10f-a626466e9847
ms.date: 12/05/2018
ms.keywords: WSD_PROBE, WSD_PROBE structure, ncd.wsd_probe_struct, wsdtypes/WSD_PROBE
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
req.typenames: WSD_PROBE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PROBE
 - wsdtypes/_WSD_PROBE
 - WSD_PROBE
 - wsdtypes/WSD_PROBE
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
 - WSD_PROBE
---

# WSD_PROBE structure


## -description

Represents a <a href="/windows/desktop/WsdApi/probe-message">Probe</a> message.

## -struct-fields

### -field Types

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.

### -field Scopes

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_scopes">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/probe-message">Probe Message</a>



<a href="/windows/desktop/WsdApi/probematches-message">ProbeMatches Message</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match">WSD_PROBE_MATCH</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_matches">WSD_PROBE_MATCHES</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match_list">WSD_PROBE_MATCH_LIST</a>