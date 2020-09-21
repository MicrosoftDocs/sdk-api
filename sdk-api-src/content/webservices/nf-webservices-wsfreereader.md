---
UID: NF:webservices.WsFreeReader
title: WsFreeReader function (webservices.h)
description: Releases the memory resource associated with an XML_Reader object.
helpviewer_keywords: ["WsFreeReader","WsFreeReader function [Web Services for Windows]","webservices/WsFreeReader","wsw.wsfreereader"]
old-location: wsw\wsfreereader.htm
tech.root: wsw
ms.assetid: 31163bea-266f-43a3-bdf5-61386ebc197c
ms.date: 12/05/2018
ms.keywords: WsFreeReader, WsFreeReader function [Web Services for Windows], webservices/WsFreeReader, wsw.wsfreereader
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
 - WsFreeReader
 - webservices/WsFreeReader
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
 - WsFreeReader
---

# WsFreeReader function


## -description

Releases the memory resource associated with  an XML_Reader object.

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> object to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a>    and the referenced <b>XML Reader</b> value may not be <b>NULL</b>.