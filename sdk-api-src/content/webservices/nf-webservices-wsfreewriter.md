---
UID: NF:webservices.WsFreeWriter
title: WsFreeWriter function (webservices.h)
description: Releases the memory resource associated with an XML Writer object.
helpviewer_keywords: ["WsFreeWriter","WsFreeWriter function [Web Services for Windows]","webservices/WsFreeWriter","wsw.wsfreewriter"]
old-location: wsw\wsfreewriter.htm
tech.root: wsw
ms.assetid: eb1eb835-838a-41e4-9e7d-c5c805237f65
ms.date: 12/05/2018
ms.keywords: WsFreeWriter, WsFreeWriter function [Web Services for Windows], webservices/WsFreeWriter, wsw.wsfreewriter
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsFreeWriter
 - webservices/WsFreeWriter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeWriter
---

# WsFreeWriter function


## -description

Releases the memory resource associated with  an  XML Writer object.

## -parameters

### -param writer [in]

A pointer to the <b>XML Writer</b> object to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a> and   the referenced value may not be <b>NULL</b>.

## -remarks

If necessary, <a href="/windows/desktop/api/webservices/nf-webservices-wsflushwriter">WsFlushWriter</a> should be called before calling <b>WsFreeWriter</b> to guarantee
        all data is emitted.