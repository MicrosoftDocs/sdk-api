---
UID: NE:mfobjects._MFVideoLighting
title: MFVideoLighting (mfobjects.h)
author: windows-sdk-content
description: Describes the optimal lighting for viewing a particular set of video content.
old-location: mf\mfvideolighting.htm
tech.root: medfound
ms.assetid: 2eeca357-b7e2-40b1-b19f-2e12a833c1ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2eeca357-b7e2-40b1-b19f-2e12a833c1ca, MFVideoLighting, MFVideoLighting enumeration [Media Foundation], MFVideoLighting_ForceDWORD, MFVideoLighting_Last, MFVideoLighting_Unknown, MFVideoLighting_bright, MFVideoLighting_dark, MFVideoLighting_dim, MFVideoLighting_office, mf.mfvideolighting, mfobjects/MFVideoLighting, mfobjects/MFVideoLighting_ForceDWORD, mfobjects/MFVideoLighting_Last, mfobjects/MFVideoLighting_Unknown, mfobjects/MFVideoLighting_bright, mfobjects/MFVideoLighting_dark, mfobjects/MFVideoLighting_dim, mfobjects/MFVideoLighting_office
ms.topic: enum
f1_keywords: 
 - "mfobjects/MFVideoLighting"
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFVideoLighting
targetos: Windows
req.typenames: MFVideoLighting
req.redist: 
ms.custom: 19H1
---

# MFVideoLighting enumeration


## -description



Describes the optimal lighting for viewing a particular set of video content.




## -enum-fields




### -field MFVideoLighting_Unknown

The optimal lighting is unknown.


### -field MFVideoLighting_bright

Bright lighting; for example, outdoors.


### -field MFVideoLighting_office

Medium brightness; for example, normal office lighting.


### -field MFVideoLighting_dim

Dim; for example, a living room with a television and additional low lighting.


### -field MFVideoLighting_dark

Dark; for example, a movie theater.


### -field MFVideoLighting_Last

Reserved.


### -field MFVideoLighting_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.


## -remarks



This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-video-lighting-attribute">MF_MT_VIDEO_LIGHTING</a> attribute.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-media-types">Video Media Types</a>
 

 

