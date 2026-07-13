---
UID: NE:wldp.WLDP_EXECUTION_POLICY
tech.root: security
title: WLDP_EXECUTION_POLICY
ms.date: 08/23/2022
targetos: Windows
description: 
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wldp.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11, Build 22621
req.target-min-winversvr: Windows 11, Build 22621
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wldp.h
api_name:
 - WLDP_EXECUTION_POLICY
f1_keywords:
 - WLDP_EXECUTION_POLICY
 - wldp/WLDP_EXECUTION_POLICY
dev_langs:
 - c++
helpviewer_keywords:
 - WLDP_EXECUTION_POLICY
---

## -description

Specifies result values for execution authorization queries with [WldpCanExecuteBuffer](nf-wldp-wldpcanexecutebuffer.md), [WldpCanExecuteFile](nf-wldp-wldpcanexecutefile.md), and [WldpCanExecuteStream](nf-wldp-wldpcanexecutestream.md).

## -enum-fields

### -field WLDP_EXECUTION_POLICY_BLOCKED

The subject does not pass execution policy and should not be executed.

### -field WLDP_EXECUTION_POLICY_ALLOWED

The subject passes execution policy and should be executed normally

### -field WLDP_EXECUTION_POLICY_REQUIRE_SANDBOX

While the subject does not pass execution policy, the execution policy allows for execution in a sandbox-like mode if one is available for the host. If a sandbox mode is available for the host, the script may be executed in that mode. Otherwise, the execution of the subject should be aborted.

## -remarks

## -see-also

