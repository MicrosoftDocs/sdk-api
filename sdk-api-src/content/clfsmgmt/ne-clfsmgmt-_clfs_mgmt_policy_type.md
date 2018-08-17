---
UID: NE:clfsmgmt._CLFS_MGMT_POLICY_TYPE
title: "_CLFS_MGMT_POLICY_TYPE"
author: windows-sdk-content
description: The CLFS_MGMT_POLICY_TYPE enumeration lists the valid policy types.
old-location: fs\clfs_mgmt_policy_type.htm
old-project: Clfs
ms.assetid: eaa817be-04ac-48c2-b7de-60509b1f65c7
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "*PCLFS_MGMT_POLICY_TYPE, CLFS_MGMT_POLICY_TYPE, CLFS_MGMT_POLICY_TYPE enumeration [Files], ClfsMgmtPolicyAutoGrow, ClfsMgmtPolicyAutoShrink, ClfsMgmtPolicyGrowthRate, ClfsMgmtPolicyLogTail, ClfsMgmtPolicyMaximumSize, ClfsMgmtPolicyMinimumSize, ClfsMgmtPolicyNewContainerExtension, ClfsMgmtPolicyNewContainerPrefix, ClfsMgmtPolicyNewContainerSize, ClfsMgmtPolicyNewContainerSuffix, PCLFS_MGMT_POLICY_TYPE, PCLFS_MGMT_POLICY_TYPE enumeration pointer [Files], _CLFS_MGMT_POLICY_TYPE, clfsmgmt/CLFS_MGMT_POLICY_TYPE, clfsmgmt/ClfsMgmtPolicyAutoGrow, clfsmgmt/ClfsMgmtPolicyAutoShrink, clfsmgmt/ClfsMgmtPolicyGrowthRate, clfsmgmt/ClfsMgmtPolicyLogTail, clfsmgmt/ClfsMgmtPolicyMaximumSize, clfsmgmt/ClfsMgmtPolicyMinimumSize, clfsmgmt/ClfsMgmtPolicyNewContainerExtension, clfsmgmt/ClfsMgmtPolicyNewContainerPrefix, clfsmgmt/ClfsMgmtPolicyNewContainerSize, clfsmgmt/ClfsMgmtPolicyNewContainerSuffix, clfsmgmt/PCLFS_MGMT_POLICY_TYPE, fs.clfs_mgmt_policy_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clfsmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CLFS_MGMT_POLICY_TYPE, *PCLFS_MGMT_POLICY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfsmgmt.h
api_name:
 - CLFS_MGMT_POLICY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLFS_MGMT_POLICY_TYPE enumeration


## -description


The <b>CLFS_MGMT_POLICY_TYPE</b> enumeration lists the valid policy types.


## -enum-fields




### -field ClfsMgmtPolicyMaximumSize

Specifies the maximum size of the log.


### -field ClfsMgmtPolicyMinimumSize

Specifies the minimum size of the log.


### -field ClfsMgmtPolicyNewContainerSize

Specifies the size of a new container.


### -field ClfsMgmtPolicyGrowthRate

Controls the rate of growth of the log. 


### -field ClfsMgmtPolicyLogTail

Controls the amount of space that   <a href="https://msdn.microsoft.com/en-us/library/Bb540390(v=VS.85).aspx">LOG_TAIL_ADVANCE_CALLBACK</a> requests.


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




<a href="https://msdn.microsoft.com/en-us/library/Bb540351(v=VS.85).aspx">CLFS_MGMT_POLICY</a>
 

 

