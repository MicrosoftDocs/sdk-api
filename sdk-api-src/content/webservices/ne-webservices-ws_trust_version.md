---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



