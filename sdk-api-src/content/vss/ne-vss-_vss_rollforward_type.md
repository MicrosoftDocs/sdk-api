---
UID: NE:vss._VSS_ROLLFORWARD_TYPE
title: "_VSS_ROLLFORWARD_TYPE"
author: windows-sdk-content
description: The VSS_ROLLFORWARD_TYPE enumeration is used by a requester to indicate the type of roll-forward operation it is about to perform.
old-location: base\vss_rollforward_type.htm
old-project: VSS
ms.assetid: 3a1f3123-659f-48e1-864d-d5abee64f819
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PVSS_ROLLFORWARD_TYPE, PVSS_ROLLFORWARD_TYPE, PVSS_ROLLFORWARD_TYPE enumeration pointer, VSS_RF_ALL, VSS_RF_NONE, VSS_RF_PARTIAL, VSS_RF_UNDEFINED, VSS_ROLLFORWARD_TYPE, VSS_ROLLFORWARD_TYPE enumeration, _VSS_ROLLFORWARD_TYPE, base.vss_rollforward_type, vss/PVSS_ROLLFORWARD_TYPE, vss/VSS_RF_ALL, vss/VSS_RF_NONE, vss/VSS_RF_PARTIAL, vss/VSS_RF_UNDEFINED, vss/VSS_ROLLFORWARD_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_ROLLFORWARD_TYPE, *PVSS_ROLLFORWARD_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_ROLLFORWARD_TYPE
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_ROLLFORWARD_TYPE enumeration


## -description


The <b>VSS_ROLLFORWARD_TYPE</b> enumeration is used by a 
    requester to indicate the type of roll-forward operation it is about to perform.


## -enum-fields




### -field VSS_RF_UNDEFINED

No roll-forward type is defined. 
      

This indicates an error on the part of the requester.


### -field VSS_RF_NONE

The roll-forward operation should not roll forward through logs.


### -field VSS_RF_ALL

The roll-forward operation should roll forward through all logs.


### -field VSS_RF_PARTIAL

The roll-forward operation should roll forward through logs up to a specified restore point.


## -remarks



A requester sets the roll-forward operation type and specifies the restore point for partial roll-forward operations using 
    <a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>.




## -see-also




<a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>
 

 

