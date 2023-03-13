---
UID: NE:davclnt.AUTHNEXTSTEP
title: AUTHNEXTSTEP (davclnt.h)
description: Specifies the next action that the WebDAV client should take after a successful call to the DavAuthCallback callback function.
helpviewer_keywords: ["AUTHNEXTSTEP","AUTHNEXTSTEP enumeration [WebDAV]","CancelRequest","DefaultBehavior","RetryRequest","davclnt/AUTHNEXTSTEP","davclnt/CancelRequest","davclnt/DefaultBehavior","davclnt/RetryRequest","webdav.authnextstep"]
old-location: webdav\authnextstep.htm
tech.root: WebDAV
ms.assetid: e9ce9e61-c395-4f6b-843c-c1caa13ac3b4
ms.date: 12/05/2018
ms.keywords: AUTHNEXTSTEP, AUTHNEXTSTEP enumeration [WebDAV], CancelRequest, DefaultBehavior, RetryRequest, davclnt/AUTHNEXTSTEP, davclnt/CancelRequest, davclnt/DefaultBehavior, davclnt/RetryRequest, webdav.authnextstep
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP2 [desktop apps only]
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
req.typenames: AUTHNEXTSTEP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AUTHNEXTSTEP
 - davclnt/AUTHNEXTSTEP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - davclnt.h
api_name:
 - AUTHNEXTSTEP
---

# AUTHNEXTSTEP enumeration


## -description

Specifies the next action that the WebDAV client should take after  a successful call to the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

## -enum-fields

### -field DefaultBehavior

Retry the connection request without using the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function. This is the same as the default behavior if no callback function is registered.

### -field RetryRequest

Retry the connection request using the credentials that were retrieved by the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> function.

### -field CancelRequest

Cancel the connection request.

## -remarks

This enumeration provides the values for the <i>NextStep</i> parameter of the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

