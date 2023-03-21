---
UID: NS:ntsecapi._LSA_LAST_INTER_LOGON_INFO
title: LSA_LAST_INTER_LOGON_INFO (ntsecapi.h)
description: Contains information about a logon session. (LSA_LAST_INTER_LOGON_INFO)
helpviewer_keywords: ["*PLSA_LAST_INTER_LOGON_INFO","LSA_LAST_INTER_LOGON_INFO","LSA_LAST_INTER_LOGON_INFO structure [Security]","PLSA_LAST_INTER_LOGON_INFO","PLSA_LAST_INTER_LOGON_INFO structure pointer [Security]","_LSA_LAST_INTER_LOGON_INFO","ntsecapi/LSA_LAST_INTER_LOGON_INFO","ntsecapi/PLSA_LAST_INTER_LOGON_INFO","security.lsa_last_inter_logon_info"]
old-location: security\lsa_last_inter_logon_info.htm
tech.root: security
ms.assetid: FB935FED-571F-4298-8F83-0F805408179D
ms.date: 12/05/2018
ms.keywords: '*PLSA_LAST_INTER_LOGON_INFO, LSA_LAST_INTER_LOGON_INFO, LSA_LAST_INTER_LOGON_INFO structure [Security], PLSA_LAST_INTER_LOGON_INFO, PLSA_LAST_INTER_LOGON_INFO structure pointer [Security], _LSA_LAST_INTER_LOGON_INFO, ntsecapi/LSA_LAST_INTER_LOGON_INFO, ntsecapi/PLSA_LAST_INTER_LOGON_INFO, security.lsa_last_inter_logon_info'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: LSA_LAST_INTER_LOGON_INFO, *PLSA_LAST_INTER_LOGON_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_LAST_INTER_LOGON_INFO
 - ntsecapi/_LSA_LAST_INTER_LOGON_INFO
 - PLSA_LAST_INTER_LOGON_INFO
 - ntsecapi/PLSA_LAST_INTER_LOGON_INFO
 - LSA_LAST_INTER_LOGON_INFO
 - ntsecapi/LSA_LAST_INTER_LOGON_INFO
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
 - LSA_LAST_INTER_LOGON_INFO
---

# LSA_LAST_INTER_LOGON_INFO structure


## -description

The <b>LSA_LAST_INTER_LOGON_INFO</b> structure contains information about a <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

## -struct-fields

### -field LastSuccessfulLogon

The time that the session owner most recently logged on  successfully.

### -field LastFailedLogon

The time of the most recent failed attempt to log on.

### -field FailedAttemptCountSinceLastSuccessfulLogon

The number of failed attempts to log on since the last successful log on.
