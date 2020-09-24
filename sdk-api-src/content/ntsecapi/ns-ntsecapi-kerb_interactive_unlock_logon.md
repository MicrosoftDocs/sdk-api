---
UID: NS:ntsecapi._KERB_INTERACTIVE_UNLOCK_LOGON
title: KERB_INTERACTIVE_UNLOCK_LOGON (ntsecapi.h)
description: Contains information used to unlock a workstation that has been locked during an interactive logon session.
helpviewer_keywords: ["*PKERB_INTERACTIVE_UNLOCK_LOGON","KERB_INTERACTIVE_UNLOCK_LOGON","KERB_INTERACTIVE_UNLOCK_LOGON structure [Security]","PKERB_INTERACTIVE_UNLOCK_LOGON","PKERB_INTERACTIVE_UNLOCK_LOGON structure pointer [Security]","ntsecapi/KERB_INTERACTIVE_UNLOCK_LOGON","ntsecapi/PKERB_INTERACTIVE_UNLOCK_LOGON","security.kerb_interactive_unlock_logon"]
old-location: security\kerb_interactive_unlock_logon.htm
tech.root: security
ms.assetid: 211d89e9-36a6-4177-8eea-d01eca320718
ms.date: 12/05/2018
ms.keywords: '*PKERB_INTERACTIVE_UNLOCK_LOGON, KERB_INTERACTIVE_UNLOCK_LOGON, KERB_INTERACTIVE_UNLOCK_LOGON structure [Security], PKERB_INTERACTIVE_UNLOCK_LOGON, PKERB_INTERACTIVE_UNLOCK_LOGON structure pointer [Security], ntsecapi/KERB_INTERACTIVE_UNLOCK_LOGON, ntsecapi/PKERB_INTERACTIVE_UNLOCK_LOGON, security.kerb_interactive_unlock_logon'
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
targetos: Windows
req.typenames: KERB_INTERACTIVE_UNLOCK_LOGON, *PKERB_INTERACTIVE_UNLOCK_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_INTERACTIVE_UNLOCK_LOGON
 - ntsecapi/_KERB_INTERACTIVE_UNLOCK_LOGON
 - PKERB_INTERACTIVE_UNLOCK_LOGON
 - ntsecapi/PKERB_INTERACTIVE_UNLOCK_LOGON
 - KERB_INTERACTIVE_UNLOCK_LOGON
 - ntsecapi/KERB_INTERACTIVE_UNLOCK_LOGON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_INTERACTIVE_UNLOCK_LOGON
---

# KERB_INTERACTIVE_UNLOCK_LOGON structure


## -description

The <b>KERB_INTERACTIVE_UNLOCK_LOGON</b> structure contains information used to unlock a workstation that has been locked during an interactive <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

## -struct-fields

### -field Logon

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a> structure that specifies the interactive logon session. The <b>MessageType</b> member of the <b>KERB_INTERACTIVE_LOGON</b> structure must be set to <b>KerbWorkstationUnlockLogon</b>.

### -field LogonId

A <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure that contains the identity of the user attempting to unlock the workstation.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a>