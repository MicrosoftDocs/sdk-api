---
UID: NS:wsdtypes._WSD_HEADER_RELATESTO
title: WSD_HEADER_RELATESTO (wsdtypes.h)
description: Represents a RelatesTo SOAP envelope header block, as specified by the WS-Addressing specification.
helpviewer_keywords: ["WSD_HEADER_RELATESTO","WSD_HEADER_RELATESTO structure","ncd.wsd_header_relatesto","ncd.wsd_header_relayesto","wsdtypes/WSD_HEADER_RELATESTO"]
old-location: ncd\wsd_header_relatesto.htm
tech.root: ncd
ms.assetid: 6085620e-2e3d-4e77-90cd-7cb9fd2c197e
ms.date: 12/05/2018
ms.keywords: WSD_HEADER_RELATESTO, WSD_HEADER_RELATESTO structure, ncd.wsd_header_relatesto, ncd.wsd_header_relayesto, wsdtypes/WSD_HEADER_RELATESTO
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
req.typenames: WSD_HEADER_RELATESTO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_HEADER_RELATESTO
 - wsdtypes/_WSD_HEADER_RELATESTO
 - WSD_HEADER_RELATESTO
 - wsdtypes/WSD_HEADER_RELATESTO
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
 - WSD_HEADER_RELATESTO
---

# WSD_HEADER_RELATESTO structure


## -description

Represents a RelatesTo SOAP envelope header block, as specified by the WS-Addressing specification.

## -struct-fields

### -field RelationshipType

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that contains the relationship type as a qualified name.

### -field MessageID

The identifier of the related message.