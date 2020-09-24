---
UID: NS:clfsmgmt._CLFS_MGMT_POLICY
title: CLFS_MGMT_POLICY (clfsmgmt.h)
description: The CLFS_MGMT_POLICY structure specifies a Common Log File System (CLFS) management policy. The PolicyType member specifies the members used for a policy.
helpviewer_keywords: ["*PCLFS_MGMT_POLICY","CLFS_MGMT_POLICY","CLFS_MGMT_POLICY structure [Files]","PCLFS_MGMT_POLICY","PCLFS_MGMT_POLICY structure pointer [Files]","clfsmgmt/CLFS_MGMT_POLICY","clfsmgmt/PCLFS_MGMT_POLICY","fs.clfs_mgmt_policy"]
old-location: fs\clfs_mgmt_policy.htm
tech.root: fs
ms.assetid: 3f5d9c38-b299-4102-9786-115ece5b0928
ms.date: 12/05/2018
ms.keywords: '*PCLFS_MGMT_POLICY, CLFS_MGMT_POLICY, CLFS_MGMT_POLICY structure [Files], PCLFS_MGMT_POLICY, PCLFS_MGMT_POLICY structure pointer [Files], clfsmgmt/CLFS_MGMT_POLICY, clfsmgmt/PCLFS_MGMT_POLICY, fs.clfs_mgmt_policy'
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
req.typenames: CLFS_MGMT_POLICY, *PCLFS_MGMT_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_MGMT_POLICY
 - clfsmgmt/_CLFS_MGMT_POLICY
 - PCLFS_MGMT_POLICY
 - clfsmgmt/PCLFS_MGMT_POLICY
 - CLFS_MGMT_POLICY
 - clfsmgmt/CLFS_MGMT_POLICY
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
 - CLFS_MGMT_POLICY
---

# CLFS_MGMT_POLICY structure


## -description

The <b>CLFS_MGMT_POLICY</b> structure specifies a Common Log File System (CLFS) management policy.  The <b>PolicyType</b> member specifies the members used for a policy.

## -struct-fields

### -field Version

Specifies the version of the log manager headers that the application is compiled with.

Set this to CLFS_MGMT_POLICY_VERSION.

### -field LengthInBytes

 Specifies the length of the entire structure.

### -field PolicyFlags

Reserved. Specify zero.

### -field PolicyType

Specifies the members used for a specific policy. Valid values are specified by <a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>.

### -field PolicyParameters

Specifies the specific policy this structure describes.

### -field PolicyParameters.MaximumSize

Specifies the maximum size of a log.

### -field PolicyParameters.MaximumSize.Containers

Specifies the maximum size of the log as a number of containers. There is no default maximum value.

### -field PolicyParameters.MinimumSize

Specifies the minimum size of a log.

### -field PolicyParameters.MinimumSize.Containers

Specifies the minimum size of the log as a number of containers. The minimum size is two (2) containers.

### -field PolicyParameters.NewContainerSize

Controls the size of a new container.

### -field PolicyParameters.NewContainerSize.SizeInBytes

Specifies the size, in bytes,  of any new containers created.

### -field PolicyParameters.GrowthRate

Controls the rate of growth of a log. The growth rate can be either a relative percentage or an absolute number of containers added, but not both. Valid values are zero (0) and greater. Specify zero (0) to indicate that the log is not to grow in size.

### -field PolicyParameters.GrowthRate.AbsoluteGrowthInContainers

Specifies the growth rate as an absolute number of containers. The default value of this member is two (2).

### -field PolicyParameters.GrowthRate.RelativeGrowthPercentage

Specifies the growth rate as a relative percentage. There is no default value for this member.

### -field PolicyParameters.LogTail

Controls the amount of space that <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_tail_advance_callback">LOG_TAIL_ADVANCE_CALLBACK</a> requests. The value is either a relative percentage or an absolute number of bytes, but not both. The value is always rounded up to the nearest container. Specify zero to indicate that no action is taken to advance the base log tail.

### -field PolicyParameters.LogTail.MinimumAvailablePercentage

Specifies the amount of space that is requested as a percentage of the entire log. The minimum amount requested frees up space in a container.

### -field PolicyParameters.LogTail.MinimumAvailableContainers

Specifies the amount of space that is requested as an absolute number of containers.

### -field PolicyParameters.AutoShrink

Controls the timing of the log-shrinking feature. This value represents the percent of free space that must exist to trigger the auto-shrink operation. The log cannot be shrunk to a size smaller than the value specified by the <b>ClfsMgmtPolicyMinimumSize</b> policy.

### -field PolicyParameters.AutoShrink.Percentage

Specifies the percentage to shrink the log by. There is no default value.

### -field PolicyParameters.AutoGrow

Controls the auto-grow feature. If auto-grow is enabled, the log grows according to the value of the <b>GrowthRate</b> member, and is limited by the value of the <b>MaximumSize</b> member when the log reaches a state where one or no containers are free.

### -field PolicyParameters.AutoGrow.Enabled

Specifies whether the auto-grow policy is enabled. Specify zero to disable the auto-grow policy. The default is disabled.

### -field PolicyParameters.NewContainerPrefix

Controls the prefix that is given to a new container.

### -field PolicyParameters.NewContainerPrefix.PrefixLengthInBytes

Specifies the length of <b>PrefixString</b>.

### -field PolicyParameters.NewContainerPrefix.PrefixString

Specifies the prefix string. This string should include a full path to the directory where the containers are created, and a prefix for the container name.

The default path to the container is the directory that contains the base log. The default value is "Container". The log container is created with the name &lt;Name of Log&gt;&lt;Default Prefix&gt;&lt;Number&gt;.

<div class="alert"><b>Note</b>  The Common Log File System (CLFS) determines the value of &lt;Number&gt;.</div>
<div> </div>

### -field PolicyParameters.NewContainerSuffix

Controls the suffix that is given to a new container.

### -field PolicyParameters.NewContainerSuffix.NextContainerSuffix

Specifies the suffix given to a new container.

### -field PolicyParameters.NewContainerExtension

Controls the extension that is given to a new container.

### -field PolicyParameters.NewContainerExtension.ExtensionLengthInBytes

Specifies the length of <b>ExtensionString</b>.

### -field PolicyParameters.NewContainerExtension.ExtensionString

Specifies the extension given to the container file.

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>