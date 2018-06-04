---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

