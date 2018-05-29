---
UID: NE:wmcodecdsp._MFVideoDSPMode
title: "_MFVideoDSPMode"
author: windows-sdk-content
description: Specifies the processing mode of the Video Stabilization MFT.
old-location: mf\mfvideodspmode.htm
old-project: medfound
ms.assetid: 24A5190B-6839-4CA1-ADBF-CDBF9B47C6AF
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFVideoDSPMode, MFVideoDSPMode enumeration [Media Foundation], MFVideoDSPMode_Passthrough, MFVideoDSPMode_Stabilization, _MFVideoDSPMode, mf.mfvideodspmode, wmcodecdsp/MFVideoDSPMode, wmcodecdsp/MFVideoDSPMode_Passthrough, wmcodecdsp/MFVideoDSPMode_Stabilization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wmcodecdsp.h
api_name:
-	MFVideoDSPMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _MFVideoDSPMode enumeration


## -description


Specifies the processing mode of the <a href="https://msdn.microsoft.com/BBC42190-08E4-4C3B-972A-FD30621A6CC1">Video Stabilization MFT</a>.


## -enum-fields




### -field MFVideoDSPMode_Passthrough

Pass-through mode. Video stabilization is not applied.


### -field MFVideoDSPMode_Stabilization

Video stabilization is applied.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/0D49892A-8628-4F2B-B41B-51160A19DC9B">MF_VIDEODSP_MODE</a> attribute.

In pass-through mode, the MFT does not apply any processing to the video.




## -see-also




<a href="https://msdn.microsoft.com/0D49892A-8628-4F2B-B41B-51160A19DC9B">MF_VIDEODSP_MODE</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/BBC42190-08E4-4C3B-972A-FD30621A6CC1">Video Stabilization MFT</a>
 

 

