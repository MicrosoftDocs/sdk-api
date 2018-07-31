---
UID: NE:webservices.WS_TRUST_VERSION
title: WS_TRUST_VERSION
author: windows-sdk-content
description: Defines the WS-Trust specification version to be used with message security and mixed-mode security.
old-location: wsw\ws_trust_version.htm
old-project: wsw
ms.assetid: 02a080f5-3d0d-4483-8215-bcb5b9f27b9c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_TRUST_VERSION, WS_TRUST_VERSION enumeration [Web Services for Windows], WS_TRUST_VERSION_1_3, WS_TRUST_VERSION_FEBRUARY_2005, webservices/WS_TRUST_VERSION, webservices/WS_TRUST_VERSION_1_3, webservices/WS_TRUST_VERSION_FEBRUARY_2005, wsw.ws_trust_version
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WS_TRUST_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_TRUST_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_TRUST_VERSION enumeration


## -description


Defines the WS-Trust specification version to be used with message
                security and mixed-mode security.
            


## -enum-fields




### -field WS_TRUST_VERSION_FEBRUARY_2005

WS-Trust with the specification URI of http://schemas.xmlsoap.org/ws/2005/02/trust
                


### -field WS_TRUST_VERSION_1_3

WS-Trust 1.3 with the specification URI of http://docs.oasis-open.org/ws-sx/ws-trust/200512
                


## -remarks



Windows 7 and Windows Server 2008 R2: WWSAPI only supports <a href="http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf">Ws-Trust</a> and <a href="http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf">Ws-SecureConversation</a> as defined by <a href="http://msdn.microsoft.com/en-us/library/dd357239(PROT.10).aspx">Lightweight Web Services Security Profile (LWSSP)</a>. For details regarding Microsoft's implementation please see the <a href="http://msdn.microsoft.com/en-us/library/dd341306(v=PROT.10).aspx">MESSAGE Syntax</a> section of LWSSP.



