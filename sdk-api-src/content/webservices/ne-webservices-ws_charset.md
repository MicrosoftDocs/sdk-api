---
UID: NE:webservices.__unnamed_enum_11
title: WS_CHARSET (webservices.h)
description: Identifies the character set of a document.
helpviewer_keywords: ["WS_CHARSET","WS_CHARSET enumeration [Web Services for Windows]","WS_CHARSET_AUTO","WS_CHARSET_UTF16BE","WS_CHARSET_UTF16LE","WS_CHARSET_UTF8","webservices/WS_CHARSET","webservices/WS_CHARSET_AUTO","webservices/WS_CHARSET_UTF16BE","webservices/WS_CHARSET_UTF16LE","webservices/WS_CHARSET_UTF8","wsw.ws_charset"]
old-location: wsw\ws_charset.htm
tech.root: wsw
ms.assetid: 47dadf5d-1bc7-4f93-936c-21c936bc3fc3
ms.date: 12/05/2018
ms.keywords: WS_CHARSET, WS_CHARSET enumeration [Web Services for Windows], WS_CHARSET_AUTO, WS_CHARSET_UTF16BE, WS_CHARSET_UTF16LE, WS_CHARSET_UTF8, webservices/WS_CHARSET, webservices/WS_CHARSET_AUTO, webservices/WS_CHARSET_UTF16BE, webservices/WS_CHARSET_UTF16LE, webservices/WS_CHARSET_UTF8, wsw.ws_charset
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
req.typenames: WS_CHARSET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CHARSET
 - webservices/WS_CHARSET
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
 - WS_CHARSET
---

# WS_CHARSET enumeration


## -description

Identifies the character set of a document.

## -enum-fields

### -field WS_CHARSET_AUTO:0

Specifies that the charset of a document should be determined automatically by inspecting
          the BOM (Byte Order Marks) of the document and the xml declaration if present.

### -field WS_CHARSET_UTF8:1

Specifies that the charset of a document is UTF-8.

### -field WS_CHARSET_UTF16LE:2

Specifies that the charset of a document is UTF-16LE.

### -field WS_CHARSET_UTF16BE:3

Specifies that the charset of a document is UTF-16BE.

