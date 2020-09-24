---
UID: NS:lmaccess._MSA_INFO_0
title: MSA_INFO_0 (lmaccess.h)
description: Specifies information about a managed service account.
helpviewer_keywords: ["*LPMSA_INFO_0","*PMSA_INFO_0","MSA_INFO_0","MSA_INFO_0 structure [Security]","PMSA_INFO_0","PMSA_INFO_0 structure pointer [Security]","lmaccess/MSA_INFO_0","lmaccess/PMSA_INFO_0","security.msa_info_0"]
old-location: security\msa_info_0.htm
tech.root: security
ms.assetid: 21e04ee8-98c9-4c78-9564-e07f5edaf847
ms.date: 12/05/2018
ms.keywords: '*LPMSA_INFO_0, *PMSA_INFO_0, MSA_INFO_0, MSA_INFO_0 structure [Security], PMSA_INFO_0, PMSA_INFO_0 structure pointer [Security], lmaccess/MSA_INFO_0, lmaccess/PMSA_INFO_0, security.msa_info_0'
req.header: lmaccess.h
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
req.typenames: MSA_INFO_0, *PMSA_INFO_0, *LPMSA_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSA_INFO_0
 - lmaccess/_MSA_INFO_0
 - PMSA_INFO_0
 - lmaccess/PMSA_INFO_0
 - MSA_INFO_0
 - lmaccess/MSA_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - MSA_INFO_0
---

# MSA_INFO_0 structure


## -description

Specifies information about a managed service account. This structure is used by the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netqueryserviceaccount">NetQueryServiceAccount</a> function.

## -struct-fields

### -field State

A value of the <a href="/windows/desktop/api/lmaccess/ne-lmaccess-msa_info_state">MSA_INFO_STATE</a> enumeration that indicates the state of the service account specified in the call to the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netqueryserviceaccount">NetQueryServiceAccount</a> function.