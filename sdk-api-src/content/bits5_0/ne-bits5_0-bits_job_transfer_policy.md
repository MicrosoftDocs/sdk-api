---
UID: NE:bits5_0.__MIDL___MIDL_itf_bits5_0_0000_0000_0001
title: BITS_JOB_TRANSFER_POLICY (bits5_0.h)
author: windows-sdk-content
description: Defines constants that specify ID values corresponding to BITS properties.
old-location: bits\bits_job_transfer_policy.htm
tech.root: Bits
ms.assetid: 6B321E80-333A-49F3-B36F-18652F2C92FE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BITS_JOB_TRANSFER_POLICY, BITS_JOB_TRANSFER_POLICY enumeration [BITS], BITS_JOB_TRANSFER_POLICY_ALWAYS, BITS_JOB_TRANSFER_POLICY_NOT_ROAMING, BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE, BITS_JOB_TRANSFER_POLICY_STANDARD, BITS_JOB_TRANSFER_POLICY_UNRESTRICTED, bits.bits_job_transfer_policy, bits5_0/BITS_JOB_TRANSFER_POLICY, bits5_0/BITS_JOB_TRANSFER_POLICY_ALWAYS, bits5_0/BITS_JOB_TRANSFER_POLICY_NOT_ROAMING, bits5_0/BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE, bits5_0/BITS_JOB_TRANSFER_POLICY_STANDARD, bits5_0/BITS_JOB_TRANSFER_POLICY_UNRESTRICTED
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits5_0.h
api_name:
 - BITS_JOB_TRANSFER_POLICY
product: Windows
targetos: Windows
req.typenames: BITS_JOB_TRANSFER_POLICY
req.redist: 
ms.custom: 19H1
---

# BITS_JOB_TRANSFER_POLICY enumeration


## -description


Defines constants that specify ID values corresponding to BITS properties.


## -enum-fields




### -field BITS_JOB_TRANSFER_POLICY_ALWAYS

Specifies that the job will be transferred when connectivity is available, regardless of the cost.


### -field BITS_JOB_TRANSFER_POLICY_NOT_ROAMING

Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.


### -field BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE

Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.


### -field BITS_JOB_TRANSFER_POLICY_STANDARD

Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.


### -field BITS_JOB_TRANSFER_POLICY_UNRESTRICTED

Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.

