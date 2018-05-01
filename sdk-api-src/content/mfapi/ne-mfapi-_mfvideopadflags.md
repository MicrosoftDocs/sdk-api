---
UID: NE:mfapi._MFVideoPadFlags
title: "_MFVideoPadFlags"
author: windows-driver-content
description: Specifies whether to pad a video image so that it fits within a specified aspect ratio.
old-location: mf\mfvideopadflags.htm
old-project: medfound
ms.assetid: c68fdd6e-4fc9-4d70-91f0-dab70315ec21
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: MFVideoPadFlag_PAD_TO_16x9, MFVideoPadFlag_PAD_TO_4x3, MFVideoPadFlag_PAD_TO_None, MFVideoPadFlags, MFVideoPadFlags enumeration [Media Foundation], _MFVideoPadFlags, c68fdd6e-4fc9-4d70-91f0-dab70315ec21, mf.mfvideopadflags, mfapi/MFVideoPadFlag_PAD_TO_16x9, mfapi/MFVideoPadFlag_PAD_TO_4x3, mfapi/MFVideoPadFlag_PAD_TO_None, mfapi/MFVideoPadFlags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFVideoPadFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	MFVideoPadFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFVideoPadFlags enumeration


## -description



Specifies whether to pad a video image so that it fits within a specified aspect ratio.




## -enum-fields




### -field MFVideoPadFlag_PAD_TO_None

Do not pad the image.


### -field MFVideoPadFlag_PAD_TO_4x3

Pad the image so that it can be displayed in a 4×3 area.


### -field MFVideoPadFlag_PAD_TO_16x9

Pad the image so that it can be displayed in a 16×9 area.


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/d7fec5fb-a1fe-4cc9-aa27-a3af0456ea8d">MF_MT_PAD_CONTROL_FLAGS</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

