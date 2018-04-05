---
UID: NS:clfsmgmt._CLFS_MGMT_POLICY
title: "_CLFS_MGMT_POLICY"
author: windows-driver-content
description: The CLFS_MGMT_POLICY structure specifies a Common Log File System (CLFS) management policy. The PolicyType member specifies the members used for a policy.
old-location: fs\clfs_mgmt_policy.htm
old-project: Clfs
ms.assetid: 3f5d9c38-b299-4102-9786-115ece5b0928
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PCLFS_MGMT_POLICY, CLFS_MGMT_POLICY, CLFS_MGMT_POLICY structure [Files], PCLFS_MGMT_POLICY, PCLFS_MGMT_POLICY structure pointer [Files], _CLFS_MGMT_POLICY, clfsmgmt/CLFS_MGMT_POLICY, clfsmgmt/PCLFS_MGMT_POLICY, fs.clfs_mgmt_policy"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CLFS_MGMT_POLICY, *PCLFS_MGMT_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Clfsmgmt.h
api_name:
-	CLFS_MGMT_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLFS_MGMT_POLICY structure


## -description


The <b>CLFS_MGMT_POLICY</b> structure specifies a Common Log File System (CLFS) management policy.  The <b>PolicyType</b> member specifies the members used for a policy.


## -struct-fields




### -field PolicyParameters

Specifies the specific policy this structure describes.


### -field PolicyParameters.MaximumSize

See <a href="https://msdn.microsoft.com/a04657ff-4498-4330-8ca5-03db0b175539">ClfsMgmtPolicyMaximumSize</a>.


### -field PolicyParameters.MaximumSize.Containers

 


### -field PolicyParameters.MinimumSize

See <a href="https://msdn.microsoft.com/4db0250c-a836-491a-8d1b-54cf098ff5a6">ClfsMgmtPolicyMinimumSize</a>.


### -field PolicyParameters.MinimumSize.Containers

 


### -field PolicyParameters.NewContainerSize

See <a href="https://msdn.microsoft.com/c86e8d5e-1638-4026-bb73-e1f04c3b7fa8">ClfsMgmtPolicyNewContainerSize</a>.


### -field PolicyParameters.NewContainerSize.SizeInBytes

 


### -field PolicyParameters.GrowthRate

See <a href="https://msdn.microsoft.com/08e7e4d8-92b8-4df6-9497-8dd914002d1c">ClfsMgmtPolicyGrowthRate</a>.


### -field PolicyParameters.GrowthRate.AbsoluteGrowthInContainers

 


### -field PolicyParameters.GrowthRate.RelativeGrowthPercentage

 


### -field PolicyParameters.LogTail

See <a href="https://msdn.microsoft.com/22c722a7-0b17-4db2-a9c9-6b753ef652c8">ClfsMgmtPolicyLogTail</a>.


### -field PolicyParameters.LogTail.MinimumAvailablePercentage

 


### -field PolicyParameters.LogTail.MinimumAvailableContainers

 


### -field PolicyParameters.AutoShrink

See <a href="https://msdn.microsoft.com/d33bfe46-8820-4b68-9359-cb32c7110b66">ClfsMgmtPolicyAutoShrink</a>.


### -field PolicyParameters.AutoShrink.Percentage

 


### -field PolicyParameters.AutoGrow

See <a href="https://msdn.microsoft.com/d55054b7-20cc-46df-99ca-56d1a65fafc7">ClfsMgmtPolicyAutoGrow</a>.


### -field PolicyParameters.AutoGrow.Enabled

 


### -field PolicyParameters.NewContainerPrefix

See <a href="https://msdn.microsoft.com/72e1e049-b66b-4473-94a2-5f6497c89e4d">ClfsMgmtPolicyNewContainerPrefix</a>.


### -field PolicyParameters.NewContainerPrefix.PrefixLengthInBytes

 


### -field PolicyParameters.NewContainerPrefix.PrefixString

 


### -field PolicyParameters.NewContainerSuffix

See <a href="https://msdn.microsoft.com/c7eeb212-65f4-41e3-bd2f-f07c680d7be7">ClfsMgmtPolicyNewContainerSuffix</a>.


### -field PolicyParameters.NewContainerSuffix.NextContainerSuffix

 


### -field PolicyParameters.NewContainerExtension

See <a href="https://msdn.microsoft.com/97c1473c-ad12-4c7b-bda9-0fb62e822a25">ClfsMgmtPolicyNewContainerExtension</a>.


### -field PolicyParameters.NewContainerExtension.ExtensionLengthInBytes

 


### -field PolicyParameters.NewContainerExtension.ExtensionString

 


### -field Version

Specifies the version of the log manager headers that the application is compiled with.

Set this to CLFS_MGMT_POLICY_VERSION.


### -field LengthInBytes

 Specifies the length of the entire structure.


### -field PolicyFlags

Reserved. Specify zero.


### -field PolicyType

Specifies the members used for a specific policy. Valid values are specified by <a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>
 

 

