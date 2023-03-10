---
UID: NS:wsdtypes._WSD_EVENTING_EXPIRES
title: WSD_EVENTING_EXPIRES (wsdtypes.h)
description: Represents the expiration time of a WS-Eventing message.
helpviewer_keywords: ["WSD_EVENTING_EXPIRES","WSD_EVENTING_EXPIRES structure","ncd.wsd_eventing_expires","wsdtypes/WSD_EVENTING_EXPIRES"]
old-location: ncd\wsd_eventing_expires.htm
tech.root: ncd
ms.assetid: 728eacdb-3c27-4884-a9ba-34979590a57c
ms.date: 12/05/2018
ms.keywords: WSD_EVENTING_EXPIRES, WSD_EVENTING_EXPIRES structure, ncd.wsd_eventing_expires, wsdtypes/WSD_EVENTING_EXPIRES
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
req.typenames: WSD_EVENTING_EXPIRES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_EVENTING_EXPIRES
 - wsdtypes/_WSD_EVENTING_EXPIRES
 - WSD_EVENTING_EXPIRES
 - wsdtypes/WSD_EVENTING_EXPIRES
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
 - WSD_EVENTING_EXPIRES
---

# WSD_EVENTING_EXPIRES structure


## -description

Represents the expiration time of a WS-Eventing message.

## -struct-fields

### -field Duration

Reference to a <a href="/windows/desktop/api/wsdxml/ns-wsdxml-wsd_duration">WSD_DURATION</a> structure that specifies the length of time a request or response is valid.

### -field DateTime

Reference to a <a href="/windows/desktop/api/wsdxml/ns-wsdxml-wsd_datetime">WSD_DATETIME</a> structure that specifies the time that the request or response expires.