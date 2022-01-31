---
UID: NE:webservices.__unnamed_enum_57
title: WS_SECURITY_HEADER_LAYOUT (webservices.h)
description: The layout rules applied to the elements of the WS-Security security header. This setting is relevant to message security bindings and mixed-mode security bindings.
helpviewer_keywords: ["WS_SECURITY_HEADER_LAYOUT","WS_SECURITY_HEADER_LAYOUT enumeration [Web Services for Windows]","WS_SECURITY_HEADER_LAYOUT_LAX","WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST","WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST","WS_SECURITY_HEADER_LAYOUT_STRICT","webservices/WS_SECURITY_HEADER_LAYOUT","webservices/WS_SECURITY_HEADER_LAYOUT_LAX","webservices/WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST","webservices/WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST","webservices/WS_SECURITY_HEADER_LAYOUT_STRICT","wsw.ws_security_header_layout"]
old-location: wsw\ws_security_header_layout.htm
tech.root: wsw
ms.assetid: a3090e6f-1f80-4d67-b7d7-1165486dcc66
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_HEADER_LAYOUT, WS_SECURITY_HEADER_LAYOUT enumeration [Web Services for Windows], WS_SECURITY_HEADER_LAYOUT_LAX, WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST, WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST, WS_SECURITY_HEADER_LAYOUT_STRICT, webservices/WS_SECURITY_HEADER_LAYOUT, webservices/WS_SECURITY_HEADER_LAYOUT_LAX, webservices/WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST, webservices/WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST, webservices/WS_SECURITY_HEADER_LAYOUT_STRICT, wsw.ws_security_header_layout
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
req.typenames: WS_SECURITY_HEADER_LAYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_HEADER_LAYOUT
 - webservices/WS_SECURITY_HEADER_LAYOUT
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
 - WS_SECURITY_HEADER_LAYOUT
---

# WS_SECURITY_HEADER_LAYOUT enumeration


## -description

The layout rules applied to the elements of the WS-Security
security header.  This setting is relevant to message security
bindings and mixed-mode security bindings.

## -enum-fields

### -field WS_SECURITY_HEADER_LAYOUT_STRICT:1

The elements of the security header must follow a 'declare before use'
layout.  All security tokens must appear before their usage.

### -field WS_SECURITY_HEADER_LAYOUT_LAX:2

The elements of the security header can be in arbitrary order,
including security tokens appearing after usage.

### -field WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST:3

The elements of the security header can be in arbitrary order as in <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_layout">WS_SECURITY_HEADER_LAYOUT_LAX</a>, but the timestamp element must
be the first element.

### -field WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST:4

The elements of the security header can be in arbitrary order as in <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_layout">WS_SECURITY_HEADER_LAYOUT_LAX</a>, but the timestamp element must
be the last element.
