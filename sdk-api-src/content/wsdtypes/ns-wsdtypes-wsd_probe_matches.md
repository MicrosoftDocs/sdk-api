---
UID: NS:wsdtypes._WSD_PROBE_MATCHES
title: WSD_PROBE_MATCHES (wsdtypes.h)
description: Represents a ProbeMatches message.
helpviewer_keywords: ["WSD_PROBE_MATCHES","WSD_PROBE_MATCHES structure","ncd.wsd_probe_matches_struct","wsdtypes/WSD_PROBE_MATCHES"]
old-location: ncd\wsd_probe_matches_struct.htm
tech.root: ncd
ms.assetid: 41bf8dc2-903a-43d4-b63d-a34242d47288
ms.date: 12/05/2018
ms.keywords: WSD_PROBE_MATCHES, WSD_PROBE_MATCHES structure, ncd.wsd_probe_matches_struct, wsdtypes/WSD_PROBE_MATCHES
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
req.typenames: WSD_PROBE_MATCHES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PROBE_MATCHES
 - wsdtypes/_WSD_PROBE_MATCHES
 - WSD_PROBE_MATCHES
 - wsdtypes/WSD_PROBE_MATCHES
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
 - WSD_PROBE_MATCHES
---

# WSD_PROBE_MATCHES structure


## -description

Represents a  <a href="/windows/desktop/WsdApi/probematches-message">ProbeMatches</a> message.

## -struct-fields

### -field ProbeMatch

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match_list">WSD_PROBE_MATCH_LIST</a> structure that contains the list of matches to the <a href="/windows/desktop/WsdApi/probe-message">Probe</a> message.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -see-also

<a href="/windows/desktop/WsdApi/probe-message">Probe Message</a>



<a href="/windows/desktop/WsdApi/probematches-message">ProbeMatches Message</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe">WSD_PROBE</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match">WSD_PROBE_MATCH</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match_list">WSD_PROBE_MATCH_LIST</a>