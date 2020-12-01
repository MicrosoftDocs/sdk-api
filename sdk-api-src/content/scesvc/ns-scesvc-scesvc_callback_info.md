---
UID: NS:scesvc._SCESVC_CALLBACK_INFO_
title: SCESVC_CALLBACK_INFO (scesvc.h)
description: The SCESVC_CALLBACK_INFO structure contains an opaque database handle and callback function pointers to query, set, and free information.
helpviewer_keywords: ["*PSCESVC_CALLBACK_INFO","PSCESVC_CALLBACK_INFO","PSCESVC_CALLBACK_INFO structure pointer [Security]","SCESVC_CALLBACK_INFO","SCESVC_CALLBACK_INFO structure [Security]","_config_scesvc_callback_info","scesvc/PSCESVC_CALLBACK_INFO","scesvc/SCESVC_CALLBACK_INFO","security.scesvc_callback_info"]
old-location: security\scesvc_callback_info.htm
tech.root: security
ms.assetid: ff232f21-2c2f-4e5e-8b2d-e89147e2d38a
ms.date: 12/05/2018
ms.keywords: '*PSCESVC_CALLBACK_INFO, PSCESVC_CALLBACK_INFO, PSCESVC_CALLBACK_INFO structure pointer [Security], SCESVC_CALLBACK_INFO, SCESVC_CALLBACK_INFO structure [Security], _config_scesvc_callback_info, scesvc/PSCESVC_CALLBACK_INFO, scesvc/SCESVC_CALLBACK_INFO, security.scesvc_callback_info'
req.header: scesvc.h
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
req.typenames: SCESVC_CALLBACK_INFO, *PSCESVC_CALLBACK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCESVC_CALLBACK_INFO_
 - scesvc/_SCESVC_CALLBACK_INFO_
 - PSCESVC_CALLBACK_INFO
 - scesvc/PSCESVC_CALLBACK_INFO
 - SCESVC_CALLBACK_INFO
 - scesvc/SCESVC_CALLBACK_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Scesvc.h
api_name:
 - SCESVC_CALLBACK_INFO
---

# SCESVC_CALLBACK_INFO structure


## -description

The <b>SCESVC_CALLBACK_INFO</b> structure contains an opaque database handle and callback function pointers to query, set, and free information.

## -struct-fields

### -field sceHandle

Specifies the opaque handle passed to the attachment by the Security Configuration tool set. This handle is used by support functions to read information from and write information to the security database.

### -field pfQueryInfo

Pointer to a 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a> callback function that queries information in the security database.

### -field pfSetInfo

Pointer to a 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a> callback function that sets information in the security database.

### -field pfFreeInfo

Pointer to a 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_free_info">PFSCE_FREE_INFO</a> callback function that frees information in the security database.

### -field pfLogInfo

Pointer to a 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_log_info">PFSCE_LOG_INFO</a> callback function that logs messages to the configuration log file or analysis log file.

## -see-also

<a href="/windows/desktop/SecMgmt/sce-handle">SCE_HANDLE</a>