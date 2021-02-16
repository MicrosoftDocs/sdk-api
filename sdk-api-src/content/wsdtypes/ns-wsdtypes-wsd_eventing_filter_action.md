---
UID: NS:wsdtypes._WSD_EVENTING_FILTER_ACTION
title: WSD_EVENTING_FILTER_ACTION (wsdtypes.h)
description: Represents a boolean expression used for filtering events.
helpviewer_keywords: ["WSD_EVENTING_FILTER_ACTION","WSD_EVENTING_FILTER_ACTION structure","ncd.wsd_eventing_filter_action","wsdtypes/WSD_EVENTING_FILTER_ACTION"]
old-location: ncd\wsd_eventing_filter_action.htm
tech.root: ncd
ms.assetid: d6fc39ec-f57a-4b20-8c8a-7e370ee3f377
ms.date: 12/05/2018
ms.keywords: WSD_EVENTING_FILTER_ACTION, WSD_EVENTING_FILTER_ACTION structure, ncd.wsd_eventing_filter_action, wsdtypes/WSD_EVENTING_FILTER_ACTION
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
req.typenames: WSD_EVENTING_FILTER_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_EVENTING_FILTER_ACTION
 - wsdtypes/_WSD_EVENTING_FILTER_ACTION
 - WSD_EVENTING_FILTER_ACTION
 - wsdtypes/WSD_EVENTING_FILTER_ACTION
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
 - WSD_EVENTING_FILTER_ACTION
---

# WSD_EVENTING_FILTER_ACTION structure


## -description

Represents a boolean expression used for filtering events

## -struct-fields

### -field Actions

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that specifies the URIs used for filtering notifications.

## -remarks

For more information about the evaluation of action filters, see Section 6.1.1, Filtering, in the <a href="https://specs.xmlsoap.org/ws/2006/02/devprof/devicesprofile.pdf">Device Profile for Web Services</a> specification.