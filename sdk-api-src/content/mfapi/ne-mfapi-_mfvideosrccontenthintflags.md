---
UID: NE:mfapi._MFVideoSrcContentHintFlags
title: "_MFVideoSrcContentHintFlags"
author: windows-sdk-content
description: Describes the intended aspect ratio for a video stream.
old-location: mf\mfvideosrccontenthintflags.htm
old-project: medfound
ms.assetid: 6166b880-36bc-4ac3-9d66-d3dd17c29ae7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 6166b880-36bc-4ac3-9d66-d3dd17c29ae7, MFVideoSrcContentHintFlag_16x9, MFVideoSrcContentHintFlag_235_1, MFVideoSrcContentHintFlag_None, MFVideoSrcContentHintFlags, MFVideoSrcContentHintFlags enumeration [Media Foundation], _MFVideoSrcContentHintFlags, mf.mfvideosrccontenthintflags, mfapi/MFVideoSrcContentHintFlag_16x9, mfapi/MFVideoSrcContentHintFlag_235_1, mfapi/MFVideoSrcContentHintFlag_None, mfapi/MFVideoSrcContentHintFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFVideoSrcContentHintFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFVideoSrcContentHintFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFVideoSrcContentHintFlags enumeration


## -description



Describes the intended aspect ratio for a video stream.




## -enum-fields




### -field MFVideoSrcContentHintFlag_None

The aspect ratio is unknown.


### -field MFVideoSrcContentHintFlag_16x9

The source is 16×9 content encoded within a 4×3 area.


### -field MFVideoSrcContentHintFlag_235_1

The source is 2.35:1 content encoded within a 16×9 or 4×3 area.


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/6b32e257-c523-4859-8c8f-661c33810624">MF_MT_SOURCE_CONTENT_HINT</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

