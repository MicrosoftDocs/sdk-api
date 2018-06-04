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

# _VSS_PROTECTION_LEVEL enumeration


## -description


Defines the set of volume shadow copy protection levels.


## -enum-fields




### -field VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME

Specifies that I/O to the original volume must be maintained at the expense of shadow copies. This is the default protection level. Shadow copies might be deleted if both of the following conditions occur:

<ul>
<li>A write to the original volume occurs.</li>
<li>The integrity of the shadow copy cannot be maintained for some reason, such as a failure to write to the shadow copy storage area or a failure to allocate sufficient memory.</li>
</ul>

### -field VSS_PROTECTION_LEVEL_SNAPSHOT

Specifies that shadow copies must be maintained at the expense of I/O to the original volume. This protection level is called "shadow copy protection mode." All I/O to the original volume will fail if both of the following conditions occur:

<ul>
<li>A write to the original volume occurs.</li>
<li>The corresponding write to the shadow copy storage area cannot be completed for some reason, such as a failure to write to the shadow copy storage area or a failure to allocate sufficient memory.</li>
</ul>

## -remarks



When a volume is in shadow copy protection mode, requesters must set shadow copy storage area (diff area) associations using the <a href="https://msdn.microsoft.com/7b58331c-b8a2-4333-a05d-563395d5f0c2">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e5abcf69-748a-4ed6-973d-8ba49ec22ef2">IVssDifferentialSoftwareSnapshotMgmt3</a>



<a href="https://msdn.microsoft.com/a67bf9f1-135b-4881-acd1-6392f27d58e5">IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel</a>



<a href="https://msdn.microsoft.com/3f8f3a0c-5076-4ce3-aa8b-5c66ac5fa47a">IVssDifferentialSoftwareSnapshotMgmt3::SetVolumeProtectLevel</a>



<a href="https://msdn.microsoft.com/65310c38-9fad-49ed-acf4-dacfa3947130">VSS_PROTECTION_FAULT</a>



<a href="https://msdn.microsoft.com/46cdc46e-fc44-452a-8aae-e47c12deedb4">VSS_VOLUME_PROTECTION_INFO</a>
 

 

