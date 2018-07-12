---
UID: NE:mfapi._MFVideoDRMFlags
title: "_MFVideoDRMFlags"
author: windows-sdk-content
description: Specifies the type of copy protection required for a video stream.
old-location: mf\mfvideodrmflags.htm
old-project: medfound
ms.assetid: 6d218992-c1c3-4d83-b364-4c7d3b50474f
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 6d218992-c1c3-4d83-b364-4c7d3b50474f, MFVideoDRMFlag_AnalogProtected, MFVideoDRMFlag_DigitallyProtected, MFVideoDRMFlag_None, MFVideoDRMFlags, MFVideoDRMFlags enumeration [Media Foundation], _MFVideoDRMFlags, mf.mfvideodrmflags, mfapi/MFVideoDRMFlag_AnalogProtected, mfapi/MFVideoDRMFlag_DigitallyProtected, mfapi/MFVideoDRMFlag_None, mfapi/MFVideoDRMFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFVideoDRMFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFVideoDRMFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFVideoDRMFlags enumeration


## -description


Specifies the type of copy protection required for a video stream.
        


## -enum-fields




### -field MFVideoDRMFlag_None

No copy protection is required.
          


### -field MFVideoDRMFlag_AnalogProtected

Analog copy protection should be applied.
          


### -field MFVideoDRMFlag_DigitallyProtected

Digital copy protection should be applied.
          


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/fb12ba38-a4f4-44fe-bf31-e731c56bb145">MF_MT_DRM_FLAGS</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

