---
UID: NE:webservices.__unnamed_enum_52
title: WS_TRUST_VERSION (webservices.h)
description: Defines the WS-Trust specification version to be used with message security and mixed-mode security.
helpviewer_keywords: ["WS_TRUST_VERSION","WS_TRUST_VERSION enumeration [Web Services for Windows]","WS_TRUST_VERSION_1_3","WS_TRUST_VERSION_FEBRUARY_2005","webservices/WS_TRUST_VERSION","webservices/WS_TRUST_VERSION_1_3","webservices/WS_TRUST_VERSION_FEBRUARY_2005","wsw.ws_trust_version"]
old-location: wsw\ws_trust_version.htm
tech.root: wsw
ms.assetid: 02a080f5-3d0d-4483-8215-bcb5b9f27b9c
ms.date: 12/05/2018
ms.keywords: WS_TRUST_VERSION, WS_TRUST_VERSION enumeration [Web Services for Windows], WS_TRUST_VERSION_1_3, WS_TRUST_VERSION_FEBRUARY_2005, webservices/WS_TRUST_VERSION, webservices/WS_TRUST_VERSION_1_3, webservices/WS_TRUST_VERSION_FEBRUARY_2005, wsw.ws_trust_version
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
req.typenames: WS_TRUST_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_TRUST_VERSION
 - webservices/WS_TRUST_VERSION
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
 - WS_TRUST_VERSION
---

# WS_TRUST_VERSION enumeration


## -description

Defines the WS-Trust specification version to be used with message
                security and mixed-mode security.

## -enum-fields

### -field WS_TRUST_VERSION_FEBRUARY_2005:0x1

WS-Trust with the specification URI of http://schemas.xmlsoap.org/ws/2005/02/trust

### -field WS_TRUST_VERSION_1_3:0x2

WS-Trust 1.3 with the specification URI of http://docs.oasis-open.org/ws-sx/ws-trust/200512

## -remarks

Windows 7 and Windows Server 2008 R2: WWSAPI only supports <a href="http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf">Ws-Trust</a> and <a href="http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf">Ws-SecureConversation</a> as defined by <a href="/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e">Lightweight Web Services Security Profile (LWSSP)</a>. For details regarding Microsoft's implementation please see the <a href="/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed">MESSAGE Syntax</a> section of LWSSP.
