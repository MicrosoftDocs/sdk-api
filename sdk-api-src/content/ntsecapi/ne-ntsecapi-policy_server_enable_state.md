---
UID: NE:ntsecapi._POLICY_SERVER_ENABLE_STATE
title: POLICY_SERVER_ENABLE_STATE
author: windows-sdk-content
description: The POLICY_SERVER_ENABLE_STATE enumeration represents the state of the LSA server&#8212;that is, whether it is enabled or disabled. Some operations may only be performed on an enabled LSA server.
old-location: security\policy_server_enable_state.htm
tech.root: secmgmt
ms.assetid: aae5875e-ca55-4571-a9a4-684280ae8aa0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_SERVER_ENABLE_STATE, POLICY_SERVER_ENABLE_STATE, POLICY_SERVER_ENABLE_STATE enumeration [Security], PPOLICY_SERVER_ENABLE_STATE, PPOLICY_SERVER_ENABLE_STATE enumeration pointer [Security], PolicyServerDisabled, PolicyServerEnabled, _lsa_policy_server_enable_state, ntsecapi/POLICY_SERVER_ENABLE_STATE, ntsecapi/PPOLICY_SERVER_ENABLE_STATE, ntsecapi/PolicyServerDisabled, ntsecapi/PolicyServerEnabled, security.policy_server_enable_state"
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Ntsecapi.h
api_name:
 - POLICY_SERVER_ENABLE_STATE
product: Windows
targetos: Windows
req.typenames: POLICY_SERVER_ENABLE_STATE, *PPOLICY_SERVER_ENABLE_STATE
req.redist: 
---

# POLICY_SERVER_ENABLE_STATE enumeration


## -description


The <b>POLICY_SERVER_ENABLE_STATE</b> enumeration represents the state of the LSA server—that is, whether it is enabled or disabled. Some operations may only be performed on an enabled LSA server.


## -enum-fields




### -field PolicyServerEnabled

The LSA server is enabled.


### -field PolicyServerDisabled

The LSA server is disabled.

