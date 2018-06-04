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

# _IMAPI_MEDIA_PHYSICAL_TYPE enumeration


## -description


Defines values for the currently known media types supported by IMAPI.


## -enum-fields




### -field IMAPI_MEDIA_TYPE_UNKNOWN

The disc recorder contains an unknown media type or the recorder is empty.


### -field IMAPI_MEDIA_TYPE_CDROM

The drive contains CD-ROM or CD-R/RW media.


### -field IMAPI_MEDIA_TYPE_CDR

The drive contains write once (CD-R) media.


### -field IMAPI_MEDIA_TYPE_CDRW

The drive contains rewritable (CD-RW) media.


### -field IMAPI_MEDIA_TYPE_DVDROM

Either the DVD drive or DVD media is read-only.


### -field IMAPI_MEDIA_TYPE_DVDRAM

The drive contains DVD-RAM media.


### -field IMAPI_MEDIA_TYPE_DVDPLUSR

The drive contains write once media that supports the DVD plus format (DVD+R) .


### -field IMAPI_MEDIA_TYPE_DVDPLUSRW

The drive contains rewritable media that supports the DVD plus format (DVD+RW).


### -field IMAPI_MEDIA_TYPE_DVDPLUSR_DUALLAYER

The drive contains write once dual layer media that supports the DVD plus format (DVD+R DL).


### -field IMAPI_MEDIA_TYPE_DVDDASHR

The drive contains write once media that supports the DVD dash format (DVD-R).


### -field IMAPI_MEDIA_TYPE_DVDDASHRW

The drive contains rewritable media that supports the DVD dash format (DVD-RW).


### -field IMAPI_MEDIA_TYPE_DVDDASHR_DUALLAYER

The drive contains write once dual layer media that supports the DVD dash format (DVD-R DL).


### -field IMAPI_MEDIA_TYPE_DISK

The drive contains a media type that supports random-access writes. This media type supports hardware defect management that identifies and avoids using damaged tracks.  


### -field IMAPI_MEDIA_TYPE_DVDPLUSRW_DUALLAYER

The drive contains rewritable dual layer media that supports the DVD plus format (DVD+RW DL).


### -field IMAPI_MEDIA_TYPE_HDDVDROM

The drive contains high definition read only DVD media (HD DVD-ROM).


### -field IMAPI_MEDIA_TYPE_HDDVDR

The drive contains write once high definition media (HD DVD-R).


### -field IMAPI_MEDIA_TYPE_HDDVDRAM

The drive contains random access high definition media (HD DVD-RAM).


### -field IMAPI_MEDIA_TYPE_BDROM

The drive contains read only Blu-ray media (BD-ROM).


### -field IMAPI_MEDIA_TYPE_BDR

The drive contains write once Blu-ray media (BD-R).


### -field IMAPI_MEDIA_TYPE_BDRE

The drive contains rewritable Blu-ray media (BD-RE) media.


### -field IMAPI_MEDIA_TYPE_MAX

This value is the maximum value defined in IMAPI_MEDIA_PHYSICAL_TYPE.


## -remarks



The values in the range 0x00000000..0x0000FFFF inclusive are reserved for extension by Microsoft. If third parties wish to report a media type not in this list using this enumeration (for example, if implementing <a href="https://msdn.microsoft.com/6b9a80fc-6ef5-4102-9361-313d33f182ab">IDiscFormat2Data::get_CurrentPhysicalMediaType</a> to support a non-listed format) they should define values only in the range 0x00010000..0xFFFFFFFF for these media types.




## -see-also




<a href="https://msdn.microsoft.com/6b9a80fc-6ef5-4102-9361-313d33f182ab">IDiscFormat2Data::get_CurrentPhysicalMediaType</a>
 

 

