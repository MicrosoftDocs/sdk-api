---
UID: NE:clfsmgmt._CLFS_MGMT_POLICY_TYPE
title: CLFS_MGMT_POLICY_TYPE (clfsmgmt.h)
description: The CLFS_MGMT_POLICY_TYPE enumeration lists the valid policy types.
helpviewer_keywords: ["*PCLFS_MGMT_POLICY_TYPE","CLFS_MGMT_POLICY_TYPE","CLFS_MGMT_POLICY_TYPE enumeration [Files]","ClfsMgmtPolicyAutoGrow","ClfsMgmtPolicyAutoShrink","ClfsMgmtPolicyGrowthRate","ClfsMgmtPolicyLogTail","ClfsMgmtPolicyMaximumSize","ClfsMgmtPolicyMinimumSize","ClfsMgmtPolicyNewContainerExtension","ClfsMgmtPolicyNewContainerPrefix","ClfsMgmtPolicyNewContainerSize","ClfsMgmtPolicyNewContainerSuffix","PCLFS_MGMT_POLICY_TYPE","PCLFS_MGMT_POLICY_TYPE enumeration pointer [Files]","clfsmgmt/CLFS_MGMT_POLICY_TYPE","clfsmgmt/ClfsMgmtPolicyAutoGrow","clfsmgmt/ClfsMgmtPolicyAutoShrink","clfsmgmt/ClfsMgmtPolicyGrowthRate","clfsmgmt/ClfsMgmtPolicyLogTail","clfsmgmt/ClfsMgmtPolicyMaximumSize","clfsmgmt/ClfsMgmtPolicyMinimumSize","clfsmgmt/ClfsMgmtPolicyNewContainerExtension","clfsmgmt/ClfsMgmtPolicyNewContainerPrefix","clfsmgmt/ClfsMgmtPolicyNewContainerSize","clfsmgmt/ClfsMgmtPolicyNewContainerSuffix","clfsmgmt/PCLFS_MGMT_POLICY_TYPE","fs.clfs_mgmt_policy_type"]
old-location: fs\clfs_mgmt_policy_type.htm
tech.root: fs
ms.assetid: eaa817be-04ac-48c2-b7de-60509b1f65c7
ms.date: 12/05/2018
ms.keywords: '*PCLFS_MGMT_POLICY_TYPE, CLFS_MGMT_POLICY_TYPE, CLFS_MGMT_POLICY_TYPE enumeration [Files], ClfsMgmtPolicyAutoGrow, ClfsMgmtPolicyAutoShrink, ClfsMgmtPolicyGrowthRate, ClfsMgmtPolicyLogTail, ClfsMgmtPolicyMaximumSize, ClfsMgmtPolicyMinimumSize, ClfsMgmtPolicyNewContainerExtension, ClfsMgmtPolicyNewContainerPrefix, ClfsMgmtPolicyNewContainerSize, ClfsMgmtPolicyNewContainerSuffix, PCLFS_MGMT_POLICY_TYPE, PCLFS_MGMT_POLICY_TYPE enumeration pointer [Files], clfsmgmt/CLFS_MGMT_POLICY_TYPE, clfsmgmt/ClfsMgmtPolicyAutoGrow, clfsmgmt/ClfsMgmtPolicyAutoShrink, clfsmgmt/ClfsMgmtPolicyGrowthRate, clfsmgmt/ClfsMgmtPolicyLogTail, clfsmgmt/ClfsMgmtPolicyMaximumSize, clfsmgmt/ClfsMgmtPolicyMinimumSize, clfsmgmt/ClfsMgmtPolicyNewContainerExtension, clfsmgmt/ClfsMgmtPolicyNewContainerPrefix, clfsmgmt/ClfsMgmtPolicyNewContainerSize, clfsmgmt/ClfsMgmtPolicyNewContainerSuffix, clfsmgmt/PCLFS_MGMT_POLICY_TYPE, fs.clfs_mgmt_policy_type'
req.header: clfsmgmt.h
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
req.typenames: CLFS_MGMT_POLICY_TYPE, *PCLFS_MGMT_POLICY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_MGMT_POLICY_TYPE
 - clfsmgmt/_CLFS_MGMT_POLICY_TYPE
 - PCLFS_MGMT_POLICY_TYPE
 - clfsmgmt/PCLFS_MGMT_POLICY_TYPE
 - CLFS_MGMT_POLICY_TYPE
 - clfsmgmt/CLFS_MGMT_POLICY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfsmgmt.h
api_name:
 - CLFS_MGMT_POLICY_TYPE
---

# CLFS_MGMT_POLICY_TYPE enumeration


## -description

The <b>CLFS_MGMT_POLICY_TYPE</b> enumeration lists the valid policy types.

## -enum-fields

### -field ClfsMgmtPolicyMaximumSize:0x0

Specifies the maximum size of the log.

### -field ClfsMgmtPolicyMinimumSize

Specifies the minimum size of the log.

### -field ClfsMgmtPolicyNewContainerSize

Specifies the size of a new container.

### -field ClfsMgmtPolicyGrowthRate

Controls the rate of growth of the log.

### -field ClfsMgmtPolicyLogTail

Controls the amount of space that   <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_tail_advance_callback">LOG_TAIL_ADVANCE_CALLBACK</a> requests.

### -field ClfsMgmtPolicyAutoShrink

Controls the percentage of containers that are removed if the log is set to autogrow.

### -field ClfsMgmtPolicyAutoGrow

Indicates if the log should automatically shrink or grow.

### -field ClfsMgmtPolicyNewContainerPrefix

Controls the prefix given to a new container.

### -field ClfsMgmtPolicyNewContainerSuffix

Controls the suffix given to a new container.

### -field ClfsMgmtPolicyNewContainerExtension

Controls the extension given to a new container.

### -field ClfsMgmtPolicyInvalid

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_policy">CLFS_MGMT_POLICY</a>
