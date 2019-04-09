---
UID: NS:vsmgmt._VSS_VOLUME_PROTECTION_INFO
title: VSS_VOLUME_PROTECTION_INFO (vsmgmt.h)
author: windows-sdk-content
description: Contains information about a volume's shadow copy protection level.
old-location: base\vss_volume_protection_info.htm
tech.root: VSS
ms.assetid: 46cdc46e-fc44-452a-8aae-e47c12deedb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVSS_VOLUME_PROTECTION_INFO, VSS_VOLUME_PROTECTION_INFO, VSS_VOLUME_PROTECTION_INFO structure, base.vss_volume_protection_info, vsmgmt/VSS_VOLUME_PROTECTION_INFO"
ms.topic: struct
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsMgmt.h
api_name:
 - VSS_VOLUME_PROTECTION_INFO
product: Windows
targetos: Windows
req.typenames: VSS_VOLUME_PROTECTION_INFO, *PVSS_VOLUME_PROTECTION_INFO
req.redist: 
---

# VSS_VOLUME_PROTECTION_INFO structure


## -description


Contains information about a volume's shadow copy protection level.


## -struct-fields




### -field m_protectionLevel

A value from the <a href="https://msdn.microsoft.com/f4c036ac-13fb-47be-8ad8-32c65caf0a2a">VSS_PROTECTION_LEVEL</a> enumeration that specifies the target protection level for the volume.


### -field m_volumeIsOfflineForProtection

TRUE if the volume is offline due to a protection fault, or <b>FALSE</b> otherwise.


### -field m_protectionFault

A value from the <a href="https://msdn.microsoft.com/65310c38-9fad-49ed-acf4-dacfa3947130">VSS_PROTECTION_FAULT</a> enumeration that describes the shadow copy protection fault that caused the volume to go offline.


### -field m_failureStatus

The internal failure status code.


### -field m_volumeHasUnusedDiffArea

TRUE if the volume has unused shadow copy storage area files, or <b>FALSE</b> otherwise.


### -field m_reserved

Reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/e5abcf69-748a-4ed6-973d-8ba49ec22ef2">IVssDifferentialSoftwareSnapshotMgmt3</a>
 

 

