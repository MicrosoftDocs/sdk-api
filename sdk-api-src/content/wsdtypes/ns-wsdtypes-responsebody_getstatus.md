---
UID: NS:wsdtypes.RESPONSEBODY_GetStatus
title: RESPONSEBODY_GetStatus (wsdtypes.h)
description: Represents a WS-Eventing GetStatus response message.
helpviewer_keywords: ["RESPONSEBODY_GetStatus","RESPONSEBODY_GetStatus structure","ncd.responsebody_getstatus","wsdtypes/RESPONSEBODY_GetMetadata"]
old-location: ncd\responsebody_getstatus.htm
tech.root: ncd
ms.assetid: 41db6c35-b722-4b46-bfc2-7bbfe50aaa0a
ms.date: 12/05/2018
ms.keywords: RESPONSEBODY_GetStatus, RESPONSEBODY_GetStatus structure, ncd.responsebody_getstatus, wsdtypes/RESPONSEBODY_GetMetadata
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
req.typenames: RESPONSEBODY_GetStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESPONSEBODY_GetStatus
 - wsdtypes/RESPONSEBODY_GetStatus
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
 - RESPONSEBODY_GetStatus
---

# RESPONSEBODY_GetStatus structure


## -description

Represents a WS-Eventing GetStatus response message.

## -struct-fields

### -field expires

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription expires.

### -field any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

