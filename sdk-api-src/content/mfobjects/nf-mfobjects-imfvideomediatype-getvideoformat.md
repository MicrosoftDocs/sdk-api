---
UID: NF:mfobjects.IMFVideoMediaType.GetVideoFormat
title: IMFVideoMediaType::GetVideoFormat (mfobjects.h)
description: GetVideoFormat is no longer available for use as of Windows 7.
old-location: mf\imfvideomediatype_getvideoformat.htm
tech.root: medfound
ms.assetid: 2168c76e-2b83-40ad-8ac1-9b76f1a31b7b
ms.date: 12/05/2018
ms.keywords: 2168c76e-2b83-40ad-8ac1-9b76f1a31b7b, GetVideoFormat, GetVideoFormat method [Media Foundation], GetVideoFormat method [Media Foundation],IMFVideoMediaType interface, IMFVideoMediaType interface [Media Foundation],GetVideoFormat method, IMFVideoMediaType.GetVideoFormat, IMFVideoMediaType::GetVideoFormat, mf.imfvideomediatype_getvideoformat, mfobjects/IMFVideoMediaType::GetVideoFormat
ms.topic: method
f1_keywords:
- mfobjects/IMFVideoMediaType.GetVideoFormat
dev_langs:
- c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFVideoMediaType.GetVideoFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMediaType::GetVideoFormat


## -description


<p class="CCE_Message">[<b>GetVideoFormat</b> is no longer available for use as of Windows 7. Instead, use the media type attributes to get the properties of the video format.]

Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure that describes the video format.


## -parameters






## -returns



This method returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.
          




## -remarks



If you need to convert the media type into an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype">MFCreateMFVideoFormatFromMFMediaType</a>.

There are no guarantees about how long the returned pointer is valid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

