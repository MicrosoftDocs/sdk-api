---
UID: NS:wsdtypes.REQUESTBODY_Renew
title: REQUESTBODY_Renew (wsdtypes.h)
description: Represents a WS-Eventing Renew request message.
helpviewer_keywords: ["REQUESTBODY_Renew","REQUESTBODY_Renew structure","ncd.requestbody_renew_struct","wsdtypes/REQUESTBODY_Renew"]
old-location: ncd\requestbody_renew_struct.htm
tech.root: ncd
ms.assetid: 2646cfb7-e372-44d2-9d4c-fa68e0d567bb
ms.date: 12/05/2018
ms.keywords: REQUESTBODY_Renew, REQUESTBODY_Renew structure, ncd.requestbody_renew_struct, wsdtypes/REQUESTBODY_Renew
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
req.typenames: REQUESTBODY_Renew
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REQUESTBODY_Renew
 - wsdtypes/REQUESTBODY_Renew
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
 - REQUESTBODY_Renew
---

# REQUESTBODY_Renew structure


## -description

Represents a WS-Eventing Renew request message.

## -struct-fields

### -field Expires

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_eventing_expires">WSD_EVENTING_EXPIRES</a> structure that specifies when the renewed subscription will expire.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

