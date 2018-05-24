---
UID: NE:msdrmdefs._DRM_USAGEPOLICY_TYPE
title: "_DRM_USAGEPOLICY_TYPE"
author: windows-driver-content
description: Used with the DRMGetUsagePolicy and DRMSetUsagePolicy functions to specify a type of usage policy.
old-location: rm\drm_usagepolicy_type.htm
old-project: AdRms_Sdk
ms.assetid: b7486f70-36da-4868-9b50-caa37f7a7539
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRM_USAGEPOLICY_TYPE, DRM_USAGEPOLICY_TYPE enumeration [Active Directory Rights Management Services SDK 1.0], DRM_USAGEPOLICY_TYPE_BYDIGEST, DRM_USAGEPOLICY_TYPE_BYNAME, DRM_USAGEPOLICY_TYPE_BYPUBLICKEY, DRM_USAGEPOLICY_TYPE_OSEXCLUSION, _DRM_USAGEPOLICY_TYPE, msdrmdefs/DRM_USAGEPOLICY_TYPE, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYDIGEST, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYNAME, msdrmdefs/DRM_USAGEPOLICY_TYPE_BYPUBLICKEY, msdrmdefs/DRM_USAGEPOLICY_TYPE_OSEXCLUSION, rm.drm_usagepolicy_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
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
req.typenames: DRM_USAGEPOLICY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msdrmdefs.h
api_name:
-	DRM_USAGEPOLICY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

