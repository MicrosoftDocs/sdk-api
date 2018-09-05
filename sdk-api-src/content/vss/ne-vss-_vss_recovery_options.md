---
UID: NE:vss._VSS_RECOVERY_OPTIONS
title: "_VSS_RECOVERY_OPTIONS"
author: windows-sdk-content
description: Used by a requester to specify how a resynchronization operation is to be performed.
old-location: base\vss_recovery_options.htm
old-project: VSS
ms.assetid: 5e58284b-9bbc-47f7-9a44-26d7153b4a25
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PVSS_RECOVERY_OPTIONS, VSS_RECOVERY_NO_VOLUME_CHECK, VSS_RECOVERY_OPTIONS, VSS_RECOVERY_OPTIONS enumeration, VSS_RECOVERY_REVERT_IDENTITY_ALL, _VSS_RECOVERY_OPTIONS, base.vss_recovery_options, vss/VSS_RECOVERY_NO_VOLUME_CHECK, vss/VSS_RECOVERY_OPTIONS, vss/VSS_RECOVERY_REVERT_IDENTITY_ALL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vss.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VSS_RECOVERY_OPTIONS, *PVSS_RECOVERY_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_RECOVERY_OPTIONS
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_RECOVERY_OPTIONS enumeration


## -description


Used by a requester to specify how a resynchronization operation is to be performed.


## -enum-fields




### -field VSS_RECOVERY_REVERT_IDENTITY_ALL

 After the resynchronization operation is complete, the signature of each target LUN  should be identical to that of the original LUN that was used to create the shadow copy.


### -field VSS_RECOVERY_NO_VOLUME_CHECK

Volume safety checks should not be performed.


## -see-also




<a href="https://msdn.microsoft.com/2e468527-11e7-42d8-808b-2cb2eb86e0ba">IVssBackupComponentsEx3::RecoverSet</a>
 

 

