---
UID: NF:webservices.WsFreeError
title: WsFreeError function (webservices.h)
description: Releases the memory resource associated with an Error object created using WsCreateError. This releases the object and its constituent information.
helpviewer_keywords: ["WsFreeError","WsFreeError function [Web Services for Windows]","webservices/WsFreeError","wsw.wsfreeerror"]
old-location: wsw\wsfreeerror.htm
tech.root: wsw
ms.assetid: 61da7bc2-b805-4379-a6b2-1e92374be1a0
ms.date: 12/05/2018
ms.keywords: WsFreeError, WsFreeError function [Web Services for Windows], webservices/WsFreeError, wsw.wsfreeerror
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
 - WsFreeError
 - webservices/WsFreeError
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
 - WsFreeError
---

# WsFreeError function


## -description

Releases the memory resource associated with an   <b>Error</b> object created using  <a href="/windows/desktop/api/webservices/nf-webservices-wscreateerror">WsCreateError</a>.
            This releases the object and its constituent information.

## -parameters

### -param error [in]

A pointer to the <b>Error</b> object to release.  The pointer must reference a valid <b>WS_ERROR</b> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreateerror">WsCreateError</a>.  The referenced value may 
                    not be NULL.