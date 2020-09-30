---
UID: NS:iketypes.IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0_
title: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0 (iketypes.h)
description: Various statistics specific to the keying module and IP version.
helpviewer_keywords: ["IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0","IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0 structure [Filtering]","fwp.ikeext_ip_version_specific_keymodule_statistics0","iketypes/IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0"]
old-location: fwp\ikeext_ip_version_specific_keymodule_statistics0.htm
tech.root: fwp
ms.assetid: 5b5bb140-ca44-4a46-bb96-aba0b499e94f
ms.date: 12/05/2018
ms.keywords: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0, IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0 structure [Filtering], fwp.ikeext_ip_version_specific_keymodule_statistics0, iketypes/IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0_
 - iketypes/IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0_
 - IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0
 - iketypes/IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0
---

# IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0 structure


## -description

The <b>IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0</b> structure contains various statistics specific to the keying module and IP version.
[IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) is available.</div><div> </div>

## -struct-fields

### -field currentActiveMainModes

Current number of active Main Mode SAs.

### -field totalMainModesStarted

Total number of Main Mode negotiations.

### -field totalSuccessfulMainModes

Total number of successful Main Mode negotiations.

### -field totalFailedMainModes

Total number of failed Main Mode negotiations.

### -field totalResponderMainModes

Total number of Main Mode negotiations that were externally initiated by a peer.

### -field currentNewResponderMainModes

Current number of newly created responder Main Modes that are still in the initial state.

### -field currentActiveQuickModes

Current number of active Quick Mode SAs.

### -field totalQuickModesStarted

Total number of Quick Mode negotiations.

### -field totalSuccessfulQuickModes

Total number of successful Quick Mode negotiations.

### -field totalFailedQuickModes

Total number of failed Quick Mode negotiations.

### -field totalAcquires

Total number of acquires received from BFE.

### -field totalReinitAcquires

Total number of acquires that were internally reinitiated.

### -field currentActiveExtendedModes

Current number of active extended mode SAs.

### -field totalExtendedModesStarted

Total number of extended mode negotiations.

### -field totalSuccessfulExtendedModes

Total number of successful extended mode negotiations.

### -field totalFailedExtendedModes

Total number of failed extended mode negotiations.

### -field totalImpersonationExtendedModes

Total number of successful extended mode negotiations that used impersonation.

### -field totalImpersonationMainModes

Total number of successful Main Mode mode negotiations that used impersonation.