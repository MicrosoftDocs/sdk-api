---
UID: NS:ntsecapi._KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST
title: KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST (ntsecapi.h)
author: windows-sdk-content
description: Cleans up the PKINIT device credentials from the computer.
old-location: security\kerb_cleanup_machine_pkinit_creds_request.htm
tech.root: SecAuthN
ms.assetid: FBFCFD7C-BB92-4EBC-9C89-51B7B5D057F1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PKERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST structure [Security], PKERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, PKERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST structure pointer [Security], ntsecapi/KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, ntsecapi/PKERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, security.kerb_cleanup_machine_pkinit_creds_request"
ms.topic: struct
f1_keywords: ["ntsecapi/KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST"]
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST
product: Windows
targetos: Windows
req.typenames: KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST, *PKERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST
req.redist: 
ms.custom: 19H1
---

# KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST structure


## -description


The 	<b>KERB_CLEANUP_MACHINE_PKINIT_CREDS_REQUEST</b> structure cleans up the PKINIT device credentials from the computer.


## -struct-fields




### -field MessageType

The type of the message. You should set this to <b>KerbCleanupMachinePkinitCredsMessage</b>.


### -field LogonId

The logon session identifier. You should set this to SYSTEM LUID or NETWORKSERVICE LUID. TCB is required if this field is different from the caller's LUID.


## -remarks



You must clean up PKINIT device credentials for LOCAL_SYSTEM 	or NETWORK_SERVICE. When the PKINIT device credential is cleaned up, only the password credentials remain.



