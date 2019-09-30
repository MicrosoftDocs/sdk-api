---
UID: NE:mftransform._MF3DVideoOutputType
title: MF3DVideoOutputType (mftransform.h)
author: windows-sdk-content
description: Specifies how to output a 3D stereoscopic video stream.
old-location: mf\mf3dvideooutputtype.htm
tech.root: medfound
ms.assetid: A41469B3-9BBF-4664-9ABA-6894A4F94BBE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MF3DVideoOutputType, MF3DVideoOutputType enumeration [Media Foundation], MF3DVideoOutputType_BaseView, MF3DVideoOutputType_Stereo, mf.mf3dvideooutputtype, mftransform/MF3DVideoOutputType, mftransform/MF3DVideoOutputType_BaseView, mftransform/MF3DVideoOutputType_Stereo
ms.topic: enum
f1_keywords: 
 - "mftransform/MF3DVideoOutputType"
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - MF3DVideoOutputType
targetos: Windows
req.typenames: MF3DVideoOutputType
req.redist: 
ms.custom: 19H1
---

# MF3DVideoOutputType enumeration


## -description


Specifies how to  output a 3D stereoscopic video stream.


## -enum-fields




### -field MF3DVideoOutputType_BaseView

Output the base view only. Discard the other view.


### -field MF3DVideoOutputType_Stereo

Output a stereo view (two buffers).


## -remarks



This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-enable-3dvideo-output">MF_ENABLE_3DVIDEO_OUTPUT</a> attribute.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

