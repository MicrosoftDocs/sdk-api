---
UID: NS:wmsdkidl.__tagDRM_VIDEO_OUTPUT_PROTECTION_IDS
title: "__tagDRM_VIDEO_OUTPUT_PROTECTION_IDS"
author: windows-sdk-content
description: The DRM_VIDEO_OUTPUT_PROTECTION_IDS structure holds an array of DRM_VIDEO_OUTPUT_PROTECTION structures.
old-location: wmformat\drm_video_output_protection_ids.htm
old-project: wmformat
ms.assetid: 95bce5f8-5230-4b69-b4e9-3cb766edce90
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRM_VIDEO_OUTPUT_PROTECTION_IDS, DRM_VIDEO_OUTPUT_PROTECTION_IDS structure [windows Media Format], __tagDRM_VIDEO_OUTPUT_PROTECTION_IDS, structure [windows Media Format], wmformat.drm_video_output_protection_ids, wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION_IDS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Drmexternals.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DRM_VIDEO_OUTPUT_PROTECTION_IDS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmsdkidl.h
api_name:
 - DRM_VIDEO_OUTPUT_PROTECTION_IDS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __tagDRM_VIDEO_OUTPUT_PROTECTION_IDS structure


## -description



The <b>DRM_VIDEO_OUTPUT_PROTECTION_IDS</b> structure holds an array of <a href="https://msdn.microsoft.com/73c7b2ab-3680-462a-ab7f-d3270ea0127b">DRM_VIDEO_OUTPUT_PROTECTION</a> structures.




## -struct-fields




### -field cEntries

Number of elements in the array referenced by <b>rgVop</b>.


### -field rgVop

Address of an array of <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structures.


## -remarks



This structure is used as a member of the <a href="https://msdn.microsoft.com/5d14bd02-0fb5-4982-b3dc-7f8277cb852f">DRM_PLAY_OPL</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/73c7b2ab-3680-462a-ab7f-d3270ea0127b">DRM_VIDEO_OUTPUT_PROTECTION</a>



<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

