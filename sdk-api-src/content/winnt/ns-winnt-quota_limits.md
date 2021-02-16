---
UID: NS:winnt._QUOTA_LIMITS
title: QUOTA_LIMITS (winnt.h)
description: Describes the amount of system resources available to a user.
helpviewer_keywords: ["*PQUOTA_LIMITS","PQUOTA_LIMITS","PQUOTA_LIMITS structure pointer [Security]","QUOTA_LIMITS","QUOTA_LIMITS structure [Security]","_QUOTA_LIMITS","_lsa_quota_limits","security.quota_limits","winnt/PQUOTA_LIMITS","winnt/QUOTA_LIMITS"]
old-location: security\quota_limits.htm
tech.root: security
ms.assetid: 7514ec77-34b1-490d-ba21-3b6944942aa7
ms.date: 12/05/2018
ms.keywords: '*PQUOTA_LIMITS, PQUOTA_LIMITS, PQUOTA_LIMITS structure pointer [Security], QUOTA_LIMITS, QUOTA_LIMITS structure [Security], _QUOTA_LIMITS, _lsa_quota_limits, security.quota_limits, winnt/PQUOTA_LIMITS, winnt/QUOTA_LIMITS'
req.header: winnt.h
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
req.typenames: QUOTA_LIMITS, *PQUOTA_LIMITS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QUOTA_LIMITS
 - winnt/_QUOTA_LIMITS
 - PQUOTA_LIMITS
 - winnt/PQUOTA_LIMITS
 - QUOTA_LIMITS
 - winnt/QUOTA_LIMITS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - QUOTA_LIMITS
---

# QUOTA_LIMITS structure


## -description

The <b>QUOTA_LIMITS</b> structure describes the amount of system resources available to a user.

## -struct-fields

### -field PagedPoolLimit

Specifies the amount of paged pool memory assigned to the user. The paged pool is an area of system memory (physical memory used by the operating system) for objects that can be written to disk when they are not being used.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.

### -field NonPagedPoolLimit

Specifies the amount of nonpaged pool memory assigned to the user. The nonpaged pool is an area of system memory  for objects that cannot be written to disk but must remain in physical memory as long as they are allocated.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.

### -field MinimumWorkingSetSize

Specifies the minimum set size assigned to the user. The "working set" of a process is the set of memory pages currently visible to the process in physical RAM memory. These pages are present in memory when the application is running and available for an application to use without triggering a page fault.

The value set in this member is not enforced by the LSA. You should set this member to <b>NULL</b>, which causes the default value to be used.

### -field MaximumWorkingSetSize

Specifies the maximum set size assigned to the user.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.

### -field PagefileLimit

Specifies the maximum size, in bytes, of the paging file, which is a reserved space on disk that backs up committed physical memory on the computer.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.

### -field TimeLimit

Indicates the maximum amount of time the process can run.

The value set in this member is not enforced by the LSA. You should set this member to <b>NULL</b>, which causes the default value to be used.

