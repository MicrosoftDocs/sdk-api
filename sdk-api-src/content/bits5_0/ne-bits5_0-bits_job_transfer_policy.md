---
UID: NE:bits5_0.BITS_JOB_TRANSFER_POLICY
title: BITS_JOB_TRANSFER_POLICY (bits5_0.h)
description: Defines constants that specify ID values corresponding to BITS properties.
helpviewer_keywords: ["BITS_JOB_TRANSFER_POLICY","BITS_JOB_TRANSFER_POLICY enumeration [BITS]","BITS_JOB_TRANSFER_POLICY_ALWAYS","BITS_JOB_TRANSFER_POLICY_NOT_ROAMING","BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE","BITS_JOB_TRANSFER_POLICY_STANDARD","BITS_JOB_TRANSFER_POLICY_UNRESTRICTED","bits.bits_job_transfer_policy","bits5_0/BITS_JOB_TRANSFER_POLICY","bits5_0/BITS_JOB_TRANSFER_POLICY_ALWAYS","bits5_0/BITS_JOB_TRANSFER_POLICY_NOT_ROAMING","bits5_0/BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE","bits5_0/BITS_JOB_TRANSFER_POLICY_STANDARD","bits5_0/BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"]
old-location: bits\bits_job_transfer_policy.htm
tech.root: Bits
ms.assetid: 6B321E80-333A-49F3-B36F-18652F2C92FE
ms.date: 12/05/2018
ms.keywords: BITS_JOB_TRANSFER_POLICY, BITS_JOB_TRANSFER_POLICY enumeration [BITS], BITS_JOB_TRANSFER_POLICY_ALWAYS, BITS_JOB_TRANSFER_POLICY_NOT_ROAMING, BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE, BITS_JOB_TRANSFER_POLICY_STANDARD, BITS_JOB_TRANSFER_POLICY_UNRESTRICTED, bits.bits_job_transfer_policy, bits5_0/BITS_JOB_TRANSFER_POLICY, bits5_0/BITS_JOB_TRANSFER_POLICY_ALWAYS, bits5_0/BITS_JOB_TRANSFER_POLICY_NOT_ROAMING, bits5_0/BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE, bits5_0/BITS_JOB_TRANSFER_POLICY_STANDARD, bits5_0/BITS_JOB_TRANSFER_POLICY_UNRESTRICTED
req.header: bits5_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: BITS_JOB_TRANSFER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BITS_JOB_TRANSFER_POLICY
 - bits5_0/BITS_JOB_TRANSFER_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits5_0.h
api_name:
 - BITS_JOB_TRANSFER_POLICY
---

# BITS_JOB_TRANSFER_POLICY enumeration


## -description

Defines constants that specify ID values corresponding to BITS properties.

## -enum-fields

### -field BITS_JOB_TRANSFER_POLICY_ALWAYS:0x800000ff

Specifies that the job will be transferred when connectivity is available, regardless of the cost.

### -field BITS_JOB_TRANSFER_POLICY_NOT_ROAMING:0x8000007f

Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.

### -field BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE:0x8000006f

Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.

### -field BITS_JOB_TRANSFER_POLICY_STANDARD:0x80000067

Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.

### -field BITS_JOB_TRANSFER_POLICY_UNRESTRICTED:0x80000021

Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.

