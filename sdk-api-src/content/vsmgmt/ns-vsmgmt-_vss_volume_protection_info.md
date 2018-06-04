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

# _VSS_VOLUME_PROTECTION_INFO structure


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
 

 

