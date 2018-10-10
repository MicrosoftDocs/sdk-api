---
UID: NS:iketypes.IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1_
title: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1_
author: windows-sdk-content
description: Various statistics specific to the keying module (IKE, Authip, and IKEv2) and IP version.
old-location: fwp\ikeext_ip_version_specific_keymodule_statistics1.htm
tech.root: FWP
ms.assetid: 45485729-dc02-4c59-83d7-0564e943e60b
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1, IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1 structure [Filtering], IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1_, fwp.ikeext_ip_version_specific_keymodule_statistics1, iketypes/IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1
product: Windows
targetos: Windows
req.typenames: IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1
req.redist: 
---

# IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1_ structure


## -description


The <b>IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</b> structure contains various statistics specific to the keying module (IKE, Authip, and IKEv2) and IP version.
<div class="alert"><b>Note</b>  <b>IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</b> is the specific implementation of IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0 is available.</div><div> </div>

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


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

