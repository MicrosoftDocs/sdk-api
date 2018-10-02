---
UID: NS:wmsdkidl.tagWMMPEG2VIDEOINFO
title: tagWMMPEG2VIDEOINFO
author: windows-sdk-content
description: The WMMPEG2VIDEOINFO structure describes an MPEG-2 video stream.
old-location: wmformat\wmmpeg2videoinfo.htm
tech.root: wmformat
ms.assetid: e5907b04-200c-4459-971b-3680989a564f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WMMPEG2VIDEOINFO, WMMPEG2VIDEOINFO structure [windows Media Format], tagWMMPEG2VIDEOINFO, wmformat.wmmpeg2videoinfo, wmsdkidl/WMMPEG2VIDEOINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wmsdkidl.h
api_name:
 - WMMPEG2VIDEOINFO
product: Windows
targetos: Windows
req.typenames: WMMPEG2VIDEOINFO
req.redist: 
---

# tagWMMPEG2VIDEOINFO structure


## -description



The <b>WMMPEG2VIDEOINFO</b> structure describes an MPEG-2 video stream.




## -struct-fields




### -field hdr


<a href="https://msdn.microsoft.com/8da9d625-5cda-45bd-a664-7211593fab92">WMVIDEOINFOHEADER2</a> structure giving header information.


### -field dwStartTimeCode

25-bit group-of-pictures (GOP) time code at start of data. This field is not used for DVD.


### -field cbSequenceHeader

Length of the sequence header, in bytes. For DVD, set this field to zero. The sequence header is given in the <b>dwSequenceHeader</b> field.


### -field dwProfile

<b>AM_MPEG2Profile</b> enumeration type that specifies the MPEG-2 profile.


### -field dwLevel

<b>AM_MPEG2Level</b> enumeration type that specifies the MPEG-2 level.


### -field dwFlags

Flag indicating preferences. Flags are defined in Dvdmedia.h.

Set undefined bits to zero or the connection will be rejected.



### -field dwSequenceHeader

Address of a buffer that contains the sequence header, including quantization matrices and the sequence extension, if required. This field is typed as a <b>DWORD</b> array to preserve the 32-bit alignment.


## -remarks



This structure is identical to the <b>MPEG2VIDEOINFO</b> structure defined in Dvdmedia.h. For more information, see the DirectShow documentation in the DirectX SDK.




## -see-also




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

