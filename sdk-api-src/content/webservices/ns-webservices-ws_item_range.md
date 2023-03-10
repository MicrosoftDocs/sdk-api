---
UID: NS:webservices._WS_ITEM_RANGE
title: WS_ITEM_RANGE (webservices.h)
description: Defines the minimum and maximum number of items that may appear when using WS_REPEATING_ELEMENT_FIELD_MAPPING, WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING, or WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING within a WS_FIELD_DESCRIPTION.
helpviewer_keywords: ["WS_ITEM_RANGE","WS_ITEM_RANGE structure [Web Services for Windows]","webservices/WS_ITEM_RANGE","wsw.ws_item_range"]
old-location: wsw\ws_item_range.htm
tech.root: wsw
ms.assetid: 29e04edd-fa39-47d0-a24c-ef3f539ce171
ms.date: 12/05/2018
ms.keywords: WS_ITEM_RANGE, WS_ITEM_RANGE structure [Web Services for Windows], webservices/WS_ITEM_RANGE, wsw.ws_item_range
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_ITEM_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ITEM_RANGE
 - webservices/_WS_ITEM_RANGE
 - WS_ITEM_RANGE
 - webservices/WS_ITEM_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ITEM_RANGE
---

# WS_ITEM_RANGE structure


## -description

Defines the minimum and maximum number of items that may appear
                when using <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, 
                <b>WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING</b>,
                or <b>WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</b> within
                a <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.  The constraint is only
                enforced during deserialization.

## -struct-fields

### -field minItemCount

The minimum number of elements that must appear.

### -field maxItemCount

The maximum number of items that may appear.