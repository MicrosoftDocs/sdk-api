---
UID: NS:wsdtypes._WSD_PROBE_MATCH_LIST
title: WSD_PROBE_MATCH_LIST (wsdtypes.h)
description: Represents a node in a single-linked list of ProbeMatch message structures.
helpviewer_keywords: ["WSD_PROBE_MATCH_LIST","WSD_PROBE_MATCH_LIST structure","ncd.wsd_probe_match_list_struct","wsdtypes/WSD_PROBE_MATCH_LIST"]
old-location: ncd\wsd_probe_match_list_struct.htm
tech.root: ncd
ms.assetid: b7922300-1dc7-487f-b703-736cb0393f17
ms.date: 12/05/2018
ms.keywords: WSD_PROBE_MATCH_LIST, WSD_PROBE_MATCH_LIST structure, ncd.wsd_probe_match_list_struct, wsdtypes/WSD_PROBE_MATCH_LIST
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
req.typenames: WSD_PROBE_MATCH_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_PROBE_MATCH_LIST
 - wsdtypes/_WSD_PROBE_MATCH_LIST
 - WSD_PROBE_MATCH_LIST
 - wsdtypes/WSD_PROBE_MATCH_LIST
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
 - WSD_PROBE_MATCH_LIST
---

# WSD_PROBE_MATCH_LIST structure


## -description

Represents a node in a single-linked list of ProbeMatch message structures.

## -struct-fields

### -field Next

Reference to the next node in the linked list of <b>WSD_PROBE_MATCH_LIST</b> structures.

### -field Element

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match">WSD_PROBE_MATCH</a> structure that contains the ProbeMatch message referenced by this node.

## -see-also

<a href="/windows/desktop/WsdApi/probe-message">Probe Message</a>



<a href="/windows/desktop/WsdApi/probematches-message">ProbeMatches Message</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe">WSD_PROBE</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_match">WSD_PROBE_MATCH</a>



<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe_matches">WSD_PROBE_MATCHES</a>