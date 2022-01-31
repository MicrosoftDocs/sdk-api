---
UID: NE:webservices.__unnamed_enum_105
title: WS_POLICY_STATE (webservices.h)
description: The state of the policy object.
helpviewer_keywords: ["WS_POLICY_STATE","WS_POLICY_STATE enumeration [Web Services for Windows]","WS_POLICY_STATE_CREATED","WS_POLICY_STATE_FAULTED","webservices/WS_POLICY_STATE","webservices/WS_POLICY_STATE_CREATED","webservices/WS_POLICY_STATE_FAULTED","wsw.ws_policy_state"]
old-location: wsw\ws_policy_state.htm
tech.root: wsw
ms.assetid: 0f6252f4-ab99-4244-be77-92144eed4e3a
ms.date: 12/05/2018
ms.keywords: WS_POLICY_STATE, WS_POLICY_STATE enumeration [Web Services for Windows], WS_POLICY_STATE_CREATED, WS_POLICY_STATE_FAULTED, webservices/WS_POLICY_STATE, webservices/WS_POLICY_STATE_CREATED, webservices/WS_POLICY_STATE_FAULTED, wsw.ws_policy_state
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
req.typenames: WS_POLICY_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_POLICY_STATE
 - webservices/WS_POLICY_STATE
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
 - WS_POLICY_STATE
---

# WS_POLICY_STATE enumeration


## -description

The state of the policy object.

## -enum-fields

### -field WS_POLICY_STATE_CREATED:1

The initial state of the policy object.

### -field WS_POLICY_STATE_FAULTED:2

The policy object is no longer usable due to a previous error.

## -remarks

The following diagram illustrates the functions that
                cause state transitions in the policy object.
            
:::image type="content" source="./images/PolicyStates.png" border="false" alt-text="Diagram of the state transitions for a Policy object showing the functions that cause transitions between the Created and Faulted states.":::

