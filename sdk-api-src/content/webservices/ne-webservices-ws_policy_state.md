---
UID: NE:webservices.__unnamed_enum_105
title: WS_POLICY_STATE (webservices.h)
author: windows-sdk-content
description: The state of the policy object.
old-location: wsw\ws_policy_state.htm
tech.root: wsw
ms.assetid: 0f6252f4-ab99-4244-be77-92144eed4e3a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_POLICY_STATE, WS_POLICY_STATE enumeration [Web Services for Windows], WS_POLICY_STATE_CREATED, WS_POLICY_STATE_FAULTED, webservices/WS_POLICY_STATE, webservices/WS_POLICY_STATE_CREATED, webservices/WS_POLICY_STATE_FAULTED, wsw.ws_policy_state
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_POLICY_STATE
product: Windows
targetos: Windows
req.typenames: WS_POLICY_STATE
req.redist: 
---

# WS_POLICY_STATE enumeration


## -description


The state of the policy object.
            


## -enum-fields




### -field WS_POLICY_STATE_CREATED

The initial state of the policy object.
                


### -field WS_POLICY_STATE_FAULTED

The policy object is no longer usable due to a previous error.
                


## -remarks



The following diagram illustrates the functions that
                cause state transitions in the policy object.
            

<img alt="" src="./images/PolicyStates.png"/>



