---
UID: NE:mftransform._MF3DVideoOutputType
title: "_MF3DVideoOutputType"
author: windows-sdk-content
description: Specifies how to output a 3D stereoscopic video stream.
old-location: mf\mf3dvideooutputtype.htm
old-project: medfound
ms.assetid: A41469B3-9BBF-4664-9ABA-6894A4F94BBE
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MF3DVideoOutputType, MF3DVideoOutputType enumeration [Media Foundation], MF3DVideoOutputType_BaseView, MF3DVideoOutputType_Stereo, _MF3DVideoOutputType, mf.mf3dvideooutputtype, mftransform/MF3DVideoOutputType, mftransform/MF3DVideoOutputType_BaseView, mftransform/MF3DVideoOutputType_Stereo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MF3DVideoOutputType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - MF3DVideoOutputType
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF3DVideoOutputType enumeration


## -description


Specifies how to  output a 3D stereoscopic video stream.


## -enum-fields




### -field MF3DVideoOutputType_BaseView

Output the base view only. Discard the other view.


### -field MF3DVideoOutputType_Stereo

Output a stereo view (two buffers).


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39">MF_ENABLE_3DVIDEO_OUTPUT</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

