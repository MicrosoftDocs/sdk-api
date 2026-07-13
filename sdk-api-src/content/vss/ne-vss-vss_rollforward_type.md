---
UID: NE:vss._VSS_ROLLFORWARD_TYPE
title: VSS_ROLLFORWARD_TYPE (vss.h)
description: The VSS_ROLLFORWARD_TYPE enumeration is used by a requester to indicate the type of roll-forward operation it is about to perform.
helpviewer_keywords: ["*PVSS_ROLLFORWARD_TYPE","PVSS_ROLLFORWARD_TYPE","PVSS_ROLLFORWARD_TYPE enumeration pointer","VSS_RF_ALL","VSS_RF_NONE","VSS_RF_PARTIAL","VSS_RF_UNDEFINED","VSS_ROLLFORWARD_TYPE","VSS_ROLLFORWARD_TYPE enumeration","base.vss_rollforward_type","vss/PVSS_ROLLFORWARD_TYPE","vss/VSS_RF_ALL","vss/VSS_RF_NONE","vss/VSS_RF_PARTIAL","vss/VSS_RF_UNDEFINED","vss/VSS_ROLLFORWARD_TYPE"]
old-location: base\vss_rollforward_type.htm
tech.root: base
ms.assetid: 3a1f3123-659f-48e1-864d-d5abee64f819
ms.date: 12/05/2018
ms.keywords: '*PVSS_ROLLFORWARD_TYPE, PVSS_ROLLFORWARD_TYPE, PVSS_ROLLFORWARD_TYPE enumeration pointer, VSS_RF_ALL, VSS_RF_NONE, VSS_RF_PARTIAL, VSS_RF_UNDEFINED, VSS_ROLLFORWARD_TYPE, VSS_ROLLFORWARD_TYPE enumeration, base.vss_rollforward_type, vss/PVSS_ROLLFORWARD_TYPE, vss/VSS_RF_ALL, vss/VSS_RF_NONE, vss/VSS_RF_PARTIAL, vss/VSS_RF_UNDEFINED, vss/VSS_ROLLFORWARD_TYPE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_ROLLFORWARD_TYPE, *PVSS_ROLLFORWARD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_ROLLFORWARD_TYPE
 - vss/_VSS_ROLLFORWARD_TYPE
 - PVSS_ROLLFORWARD_TYPE
 - vss/PVSS_ROLLFORWARD_TYPE
 - VSS_ROLLFORWARD_TYPE
 - vss/VSS_ROLLFORWARD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_ROLLFORWARD_TYPE
---

# VSS_ROLLFORWARD_TYPE enumeration


## -description

The <b>VSS_ROLLFORWARD_TYPE</b> enumeration is used by a 
    requester to indicate the type of roll-forward operation it is about to perform.

## -enum-fields

### -field VSS_RF_UNDEFINED:0

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
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">IVssBackupComponentsEx2::SetRollForward</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">IVssBackupComponentsEx2::SetRollForward</a>
