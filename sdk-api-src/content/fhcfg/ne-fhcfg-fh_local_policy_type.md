---
UID: NE:fhcfg._FH_LOCAL_POLICY_TYPE
title: FH_LOCAL_POLICY_TYPE (fhcfg.h)
description: Specifies the type of a local policy for the File History feature. Each local policy has a numeric parameter associated with it.
helpviewer_keywords: ["*PFH_LOCAL_POLICY_TYPE","FH_FREQUENCY","FH_LOCAL_POLICY_TYPE","FH_LOCAL_POLICY_TYPE enumeration [Windows API]","FH_RETENTION_AGE","FH_RETENTION_TYPE","MAX_LOCAL_POLICY","fhcfg/FH_FREQUENCY","fhcfg/FH_LOCAL_POLICY_TYPE","fhcfg/FH_RETENTION_AGE","fhcfg/FH_RETENTION_TYPE","fhcfg/MAX_LOCAL_POLICY","winprog.fh_local_policy_type"]
old-location: winprog\fh_local_policy_type.htm
tech.root: winprog
ms.assetid: 59C54A67-91A3-495F-95F2-50EB373D442C
ms.date: 12/05/2018
ms.keywords: '*PFH_LOCAL_POLICY_TYPE, FH_FREQUENCY, FH_LOCAL_POLICY_TYPE, FH_LOCAL_POLICY_TYPE enumeration [Windows API], FH_RETENTION_AGE, FH_RETENTION_TYPE, MAX_LOCAL_POLICY, fhcfg/FH_FREQUENCY, fhcfg/FH_LOCAL_POLICY_TYPE, fhcfg/FH_RETENTION_AGE, fhcfg/FH_RETENTION_TYPE, fhcfg/MAX_LOCAL_POLICY, winprog.fh_local_policy_type'
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FH_LOCAL_POLICY_TYPE, *PFH_LOCAL_POLICY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_LOCAL_POLICY_TYPE
 - fhcfg/_FH_LOCAL_POLICY_TYPE
 - PFH_LOCAL_POLICY_TYPE
 - fhcfg/PFH_LOCAL_POLICY_TYPE
 - FH_LOCAL_POLICY_TYPE
 - fhcfg/FH_LOCAL_POLICY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_LOCAL_POLICY_TYPE
---

# FH_LOCAL_POLICY_TYPE enumeration


## -description

Specifies the type of a local policy for the File History feature. Each local policy has a numeric parameter associated with it.

## -enum-fields

### -field FH_FREQUENCY:0

This local policy specifies how frequently backups are to be performed for the current user. The numeric parameter contains the time, in seconds, from the end of one backup until the start of the next one. The default value of the numeric parameter for this policy is 3600 seconds (1 hour).

### -field FH_RETENTION_TYPE

This  local policy specifies when previous versions of files and folders can be deleted from a backup target. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_retention_types">FH_RETENTION_TYPES</a> enumeration for the list of possible values. The default value of the numeric parameter for this policy is <b>FH_RETENTION_DISABLED</b>.

### -field FH_RETENTION_AGE

This local policy specifies the minimum age of previous versions that can be deleted from a backup target when the  <b>FH_RETENTION_AGE_BASED</b> retention type is specified. For more information, see the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_retention_types">FH_RETENTION_TYPES</a> enumeration. The numeric parameter contains the minimum age, in days. The default value of the numeric parameter for this policy is 365 days (1 year).

### -field MAX_LOCAL_POLICY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.

## -remarks

To retrieve the value of the numeric parameter for a local policy, use the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">IFhConfigMgr::GetLocalPolicy</a> method.

To set the value of the numeric parameter for the local policy, use the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_retention_types">FH_RETENTION_TYPES</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">IFhConfigMgr::GetLocalPolicy</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a>
