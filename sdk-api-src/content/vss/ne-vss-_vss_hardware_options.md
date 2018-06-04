---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VSS_HARDWARE_OPTIONS enumeration


## -description


Defines shadow copy LUN flags.


## -enum-fields




### -field VSS_BREAKEX_FLAG_MASK_LUNS

The shadow copy LUN will be masked from the host.


### -field VSS_BREAKEX_FLAG_MAKE_READ_WRITE

The shadow copy LUN will be exposed to the host as a read-write volume.


### -field VSS_BREAKEX_FLAG_REVERT_IDENTITY_ALL

The disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs. However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.


### -field VSS_BREAKEX_FLAG_REVERT_IDENTITY_NONE

None of the disk identifiers of the shadow copy LUNs will be reverted.


### -field VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE

The shadow copy LUNs will be converted permanently to read-write. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.


### -field VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY

The shadow copy LUNs will be converted temporarily to read-write and are about to undergo TxF recovery or VSS auto-recovery. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.


### -field VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY

The shadow copy LUNs have just undergone TxF recovery or VSS auto-recovery and have been converted back to read-only. This flag is set only as a notification for the provider; no provider action is required. For more information, see the <a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.


### -field VSS_ONLUNSTATECHANGE_DO_MASK_LUNS

The provider must mask shadow copy LUNs from this computer. For more information, see the <a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">IVssHardwareSnapshotProviderEx::OnLunStateChange</a> method.


## -see-also




<a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">IVssHardwareSnapshotProviderEx::OnLunStateChange</a>
 

 

