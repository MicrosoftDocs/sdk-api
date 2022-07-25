---
UID: NE:txlogpub.RECORD_READING_POLICY
title: RECORD_READING_POLICY (txlogpub.h)
description: Specifies a hint about the order in which records are to be read from a log.
helpviewer_keywords: ["RECORD_READING_POLICY","RECORD_READING_POLICY enumeration [COM]","RECORD_READING_POLICY_BACKWARD","RECORD_READING_POLICY_FORWARD","RECORD_READING_POLICY_RANDOM","_com_RECORD_READING_POLICY","com.record_reading_policy","txlogpub/RECORD_READING_POLICY","txlogpub/RECORD_READING_POLICY_BACKWARD","txlogpub/RECORD_READING_POLICY_FORWARD","txlogpub/RECORD_READING_POLICY_RANDOM"]
old-location: com\record_reading_policy.htm
tech.root: com
ms.assetid: 79ffd37a-ffeb-46f8-8743-aa3e85648e34
ms.date: 12/05/2018
ms.keywords: RECORD_READING_POLICY, RECORD_READING_POLICY enumeration [COM], RECORD_READING_POLICY_BACKWARD, RECORD_READING_POLICY_FORWARD, RECORD_READING_POLICY_RANDOM, _com_RECORD_READING_POLICY, com.record_reading_policy, txlogpub/RECORD_READING_POLICY, txlogpub/RECORD_READING_POLICY_BACKWARD, txlogpub/RECORD_READING_POLICY_FORWARD, txlogpub/RECORD_READING_POLICY_RANDOM
req.header: txlogpub.h
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
req.typenames: RECORD_READING_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RECORD_READING_POLICY
 - txlogpub/RECORD_READING_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TxLogpub.h
api_name:
 - RECORD_READING_POLICY
---

# RECORD_READING_POLICY enumeration


## -description

Specifies a hint about the order in which records are to be read from a log.

## -enum-fields

### -field RECORD_READING_POLICY_FORWARD:1

Indicates that records will be read in order of increasing LSN (from least recent to most recent).

### -field RECORD_READING_POLICY_BACKWARD:2

Indicates that records will be read in order of decreasing LSN (from most recent to least recent).

### -field RECORD_READING_POLICY_RANDOM:3

Indicates that records may be read in any order.

## -see-also

<a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-setaccesspolicyhint">ILog::SetAccessPolicyHint</a>
