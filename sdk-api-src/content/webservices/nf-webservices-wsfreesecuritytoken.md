---
UID: NF:webservices.WsFreeSecurityToken
title: WsFreeSecurityToken function (webservices.h)
description: Releases the memory resource associated with a Security Token object.
helpviewer_keywords: ["WsFreeSecurityToken","WsFreeSecurityToken function [Web Services for Windows]","webservices/WsFreeSecurityToken","wsw.wsfreesecuritytoken"]
old-location: wsw\wsfreesecuritytoken.htm
tech.root: wsw
ms.assetid: 7f9500a8-b54f-4967-8f8d-9f8770d3dd60
ms.date: 12/05/2018
ms.keywords: WsFreeSecurityToken, WsFreeSecurityToken function [Web Services for Windows], webservices/WsFreeSecurityToken, wsw.wsfreesecuritytoken
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
 - WsFreeSecurityToken
 - webservices/WsFreeSecurityToken
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
 - WsFreeSecurityToken
---

# WsFreeSecurityToken function


## -description

Releases the memory resource associated with  a <b>Security Token</b> object.

## -parameters

### -param token [in]

A pointer to the <b>Security Token</b> object to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-security-token">WS_SECURITY_TOKEN</a> object returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatexmlsecuritytoken">WsCreateXmlSecurityToken</a>.