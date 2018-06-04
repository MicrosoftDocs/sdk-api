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

# SetupVerifyInfFileW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupVerifyInfFile</b> function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform.


## -parameters




### -param InfName [in]

The name of the INF file to be verified. This name may include a path.


### -param AltPlatformInfo [in]

An optional pointer to a 
<a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a> structure that contains information about the alternate platform to use when validating the INF file. This parameter can be Null.


### -param InfSignerInfo

TBD




#### - InfFileName [out]

A pointer to an <a href="https://msdn.microsoft.com/50ceee47-3a89-4bd7-8508-5a4d75514861">SP_INF_SIGNER_INFO</a> structure that receives information about the INF digital signature, that is, if it is signed.


## -returns



This function returns WINSETUPAPI BOOL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

