---
UID: NE:imapi2._IMAPI_MEDIA_PHYSICAL_TYPE
title: "_IMAPI_MEDIA_PHYSICAL_TYPE"
author: windows-driver-content
description: Defines values for the currently known media types supported by IMAPI.
old-location: imapi\imapi_media_physical_type.htm
old-project: imapi
ms.assetid: 027c5e09-6cf7-4d7c-8381-07dc92cc43c5
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PIMAPI_MEDIA_PHYSICAL_TYPE, IMAPI_MEDIA_PHYSICAL_TYPE, IMAPI_MEDIA_PHYSICAL_TYPE enumeration [IMAPI], IMAPI_MEDIA_TYPE_BDR, IMAPI_MEDIA_TYPE_BDRE, IMAPI_MEDIA_TYPE_BDROM, IMAPI_MEDIA_TYPE_CDR, IMAPI_MEDIA_TYPE_CDROM, IMAPI_MEDIA_TYPE_CDRW, IMAPI_MEDIA_TYPE_DISK, IMAPI_MEDIA_TYPE_DVDDASHR, IMAPI_MEDIA_TYPE_DVDDASHRW, IMAPI_MEDIA_TYPE_DVDDASHR_DUALLAYER, IMAPI_MEDIA_TYPE_DVDPLUSR, IMAPI_MEDIA_TYPE_DVDPLUSRW, IMAPI_MEDIA_TYPE_DVDPLUSRW_DUALLAYER, IMAPI_MEDIA_TYPE_DVDPLUSR_DUALLAYER, IMAPI_MEDIA_TYPE_DVDRAM, IMAPI_MEDIA_TYPE_DVDROM, IMAPI_MEDIA_TYPE_HDDVDR, IMAPI_MEDIA_TYPE_HDDVDRAM, IMAPI_MEDIA_TYPE_HDDVDROM, IMAPI_MEDIA_TYPE_MAX, IMAPI_MEDIA_TYPE_UNKNOWN, PIMAPI_MEDIA_PHYSICAL_TYPE, PIMAPI_MEDIA_PHYSICAL_TYPE enumeration pointer [IMAPI], _IMAPI_MEDIA_PHYSICAL_TYPE, imapi.imapi_media_physical_type, imapi2/IMAPI_MEDIA_PHYSICAL_TYPE, imapi2/IMAPI_MEDIA_TYPE_BDR, imapi2/IMAPI_MEDIA_TYPE_BDRE, imapi2/IMAPI_MEDIA_TYPE_BDROM, imapi2/IMAPI_MEDIA_TYPE_CDR, imapi2/IMAPI_MEDIA_TYPE_CDROM, imapi2/IMAPI_MEDIA_TYPE_CDRW, imapi2/IMAPI_MEDIA_TYPE_DISK, imapi2/IMAPI_MEDIA_TYPE_DVDDASHR, imapi2/IMAPI_MEDIA_TYPE_DVDDASHRW, imapi2/IMAPI_MEDIA_TYPE_DVDDASHR_DUALLAYER, imapi2/IMAPI_MEDIA_TYPE_DVDPLUSR, imapi2/IMAPI_MEDIA_TYPE_DVDPLUSRW, imapi2/IMAPI_MEDIA_TYPE_DVDPLUSRW_DUALLAYER, imapi2/IMAPI_MEDIA_TYPE_DVDPLUSR_DUALLAYER, imapi2/IMAPI_MEDIA_TYPE_DVDRAM, imapi2/IMAPI_MEDIA_TYPE_DVDROM, imapi2/IMAPI_MEDIA_TYPE_HDDVDR, imapi2/IMAPI_MEDIA_TYPE_HDDVDRAM, imapi2/IMAPI_MEDIA_TYPE_HDDVDROM, imapi2/IMAPI_MEDIA_TYPE_MAX, imapi2/IMAPI_MEDIA_TYPE_UNKNOWN, imapi2/PIMAPI_MEDIA_PHYSICAL_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_MEDIA_PHYSICAL_TYPE, *PIMAPI_MEDIA_PHYSICAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	imapi2.h
api_name:
-	IMAPI_MEDIA_PHYSICAL_TYPE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

