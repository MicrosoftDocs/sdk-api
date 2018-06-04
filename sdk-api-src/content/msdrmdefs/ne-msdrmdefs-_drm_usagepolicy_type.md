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

# _DRM_USAGEPOLICY_TYPE enumeration


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRM_USAGEPOLICY_TYPE</b> enumeration is used with the <a href="https://msdn.microsoft.com/135ed2d0-17a9-46a2-9495-4102115f7bad">DRMGetUsagePolicy</a> and <a href="https://msdn.microsoft.com/8c270824-ff2a-4b04-b8b0-7cc4a82d042d">DRMSetUsagePolicy</a> functions to specify a type of usage policy.


## -enum-fields




### -field DRM_USAGEPOLICY_TYPE_BYNAME

The usage policy is tied to an application name.


### -field DRM_USAGEPOLICY_TYPE_BYPUBLICKEY

The usage policy is tied to an application's public key.


### -field DRM_USAGEPOLICY_TYPE_BYDIGEST

The usage policy is tied to a digest of an application.


### -field DRM_USAGEPOLICY_TYPE_OSEXCLUSION

The usage policy is tied to an operating system.


## -see-also




<a href="https://msdn.microsoft.com/bc3a8ab3-9f89-442b-9910-85820b2b2653">AD RMS Enumerations</a>



<a href="https://msdn.microsoft.com/135ed2d0-17a9-46a2-9495-4102115f7bad">DRMGetUsagePolicy</a>



<a href="https://msdn.microsoft.com/8c270824-ff2a-4b04-b8b0-7cc4a82d042d">DRMSetUsagePolicy</a>
 

 

