---
UID: NF:segment.IMSVidEVR.get_SuppressEffects
title: IMSVidEVR::get_SuppressEffects
author: windows-driver-content
description: The get_SuppressEffects method queries whether the Video Control configures the system for optimal video playback
old-location: mstv\imsvidevr_get_suppresseffects.htm
old-project: mstv
ms.assetid: a3aaf310-6c42-4013-a3bf-25f9c42cdf81
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],get_SuppressEffects method, IMSVidEVR.get_SuppressEffects, IMSVidEVR::get_SuppressEffects, IMSVidEVRget_SuppressEffects, get_SuppressEffects, get_SuppressEffects method [Microsoft TV Technologies], get_SuppressEffects method [Microsoft TV Technologies],IMSVidEVR interface, mstv.imsvidevr_get_suppresseffects, segment/IMSVidEVR::get_SuppressEffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidEVR.get_SuppressEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidEVR::get_SuppressEffects


## -description


The <b>get_SuppressEffects</b> method queries whether the <a href="https://msdn.microsoft.com/743a1950-4f70-45a1-9536-0d75064f401b">Video Control</a> configures the system for optimal video playback


## -parameters




### -param bSuppress [out]

Receives a <b>VARIANT_BOOL</b>. For more information, see <a href="https://msdn.microsoft.com/399250b6-4f2d-4dbf-b1e8-d32a0673617e">IMSVidEVR::put_SuppressEffects</a>. The default value is VARIANT_TRUE.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/437f515b-0353-4ff2-b8c2-5dd27d4e12f7">IMSVidEVR</a>
 

 

