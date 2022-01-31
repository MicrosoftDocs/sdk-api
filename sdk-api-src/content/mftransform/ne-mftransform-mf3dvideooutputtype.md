---
UID: NE:mftransform._MF3DVideoOutputType
title: MF3DVideoOutputType (mftransform.h)
description: Specifies how to output a 3D stereoscopic video stream.
helpviewer_keywords: ["MF3DVideoOutputType","MF3DVideoOutputType enumeration [Media Foundation]","MF3DVideoOutputType_BaseView","MF3DVideoOutputType_Stereo","mf.mf3dvideooutputtype","mftransform/MF3DVideoOutputType","mftransform/MF3DVideoOutputType_BaseView","mftransform/MF3DVideoOutputType_Stereo"]
old-location: mf\mf3dvideooutputtype.htm
tech.root: mf
ms.assetid: A41469B3-9BBF-4664-9ABA-6894A4F94BBE
ms.date: 12/05/2018
ms.keywords: MF3DVideoOutputType, MF3DVideoOutputType enumeration [Media Foundation], MF3DVideoOutputType_BaseView, MF3DVideoOutputType_Stereo, mf.mf3dvideooutputtype, mftransform/MF3DVideoOutputType, mftransform/MF3DVideoOutputType_BaseView, mftransform/MF3DVideoOutputType_Stereo
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
targetos: Windows
req.typenames: MF3DVideoOutputType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF3DVideoOutputType
 - mftransform/_MF3DVideoOutputType
 - MF3DVideoOutputType
 - mftransform/MF3DVideoOutputType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - MF3DVideoOutputType
---

# MF3DVideoOutputType enumeration


## -description

Specifies how to  output a 3D stereoscopic video stream.

## -enum-fields

### -field MF3DVideoOutputType_BaseView:0

Output the base view only. Discard the other view.

### -field MF3DVideoOutputType_Stereo:1

Output a stereo view (two buffers).

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-enable-3dvideo-output">MF_ENABLE_3DVIDEO_OUTPUT</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
