---
UID: NS:wsman._WSMAN_PROXY_INFO
title: WSMAN_PROXY_INFO (wsman.h)
description: Specifies proxy information.helpviewer_keywords: ["WSMAN_PROXY_INFO","WSMAN_PROXY_INFO structure [Windows Remote Management]","winrm.wsman_proxy_info","wsman/WSMAN_PROXY_INFO"]
old-location: winrm\wsman_proxy_info.htm
tech.root: winrm
ms.assetid: 0542fa39-c574-4a5e-b8eb-6ddf8a58600a
ms.date: 12/05/2018
ms.keywords: WSMAN_PROXY_INFO, WSMAN_PROXY_INFO structure [Windows Remote Management], winrm.wsman_proxy_info, wsman/WSMAN_PROXY_INFO
f1_keywords:
- wsman/WSMAN_PROXY_INFO
dev_langs:
- c++
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wsman.h
api_name:
- WSMAN_PROXY_INFO
targetos: Windows
req.typenames: WSMAN_PROXY_INFO
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
---

# WSMAN_PROXY_INFO structure


## -description


Specifies proxy information.


## -struct-fields




### -field accessType

Specifies the access type for the proxy. This member must be set to one of the values defined in the <a href="https://docs.microsoft.com/windows/desktop/api/wsman/ne-wsman-wsmanproxyaccesstype">WSManProxyAccessType</a> enumeration.


### -field authenticationCredentials

A <a href="https://docs.microsoft.com/windows/desktop/api/wsman/ns-wsman-wsman_authentication_credentials">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure that specifies the credentials and authentication scheme used for proxy access.

