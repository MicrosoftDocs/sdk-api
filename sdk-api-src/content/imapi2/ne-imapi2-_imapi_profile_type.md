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

# _IMAPI_PROFILE_TYPE enumeration


## -description


Defines values for the possible profiles of a CD and DVD device.  A profile defines the type of media and features that the device supports. 


## -enum-fields




### -field IMAPI_PROFILE_TYPE_INVALID

The profile is not valid.


### -field IMAPI_PROFILE_TYPE_NON_REMOVABLE_DISK

The hard disk it not removable.


### -field IMAPI_PROFILE_TYPE_REMOVABLE_DISK

The hard disk is removable.


### -field IMAPI_PROFILE_TYPE_MO_ERASABLE

An Magneto-Optical Erasable drive.


### -field IMAPI_PROFILE_TYPE_MO_WRITE_ONCE

A write once optical drive.


### -field IMAPI_PROFILE_TYPE_AS_MO

An advance storage Magneto-Optical drive.


### -field IMAPI_PROFILE_TYPE_CDROM

A CD-ROM drive.


### -field IMAPI_PROFILE_TYPE_CD_RECORDABLE

A CD-R drive.


### -field IMAPI_PROFILE_TYPE_CD_REWRITABLE

A CD-RW or CD+RW drive.


### -field IMAPI_PROFILE_TYPE_DVDROM

A DVD-ROM drive.


### -field IMAPI_PROFILE_TYPE_DVD_DASH_RECORDABLE

A DVD-R sequential recording drive.


### -field IMAPI_PROFILE_TYPE_DVD_RAM

A DVD-RAM drive.


### -field IMAPI_PROFILE_TYPE_DVD_DASH_REWRITABLE

A DVD-RW restricted overwrite drive.


### -field IMAPI_PROFILE_TYPE_DVD_DASH_RW_SEQUENTIAL

A DVD-RW sequential recording drive.


### -field IMAPI_PROFILE_TYPE_DVD_DASH_R_DUAL_SEQUENTIAL

A DVD-R dual layer sequential recording drive.


### -field IMAPI_PROFILE_TYPE_DVD_DASH_R_DUAL_LAYER_JUMP

A DVD-R dual layer jump recording drive.


### -field IMAPI_PROFILE_TYPE_DVD_PLUS_RW

A DVD+RW drive.


### -field IMAPI_PROFILE_TYPE_DVD_PLUS_R

A DVD+R drive.


### -field IMAPI_PROFILE_TYPE_DDCDROM

A double density CD drive.

<div class="alert"><b>Note</b>  This profile has been deprecated.</div>
<div> </div>

### -field IMAPI_PROFILE_TYPE_DDCD_RECORDABLE

A double density CD-R drive.

<div class="alert"><b>Note</b>  This profile has been deprecated.</div>
<div> </div>

### -field IMAPI_PROFILE_TYPE_DDCD_REWRITABLE

A double density CD-RW drive.

<div class="alert"><b>Note</b>  This profile has been deprecated.</div>
<div> </div>

### -field IMAPI_PROFILE_TYPE_DVD_PLUS_RW_DUAL

A DVD+RW dual layer drive.


### -field IMAPI_PROFILE_TYPE_DVD_PLUS_R_DUAL

A DVD+R dual layer drive.


### -field IMAPI_PROFILE_TYPE_BD_ROM

A Blu-ray read only drive.


### -field IMAPI_PROFILE_TYPE_BD_R_SEQUENTIAL

A write once Blu-ray drive with sequential recording.


### -field IMAPI_PROFILE_TYPE_BD_R_RANDOM_RECORDING

A write once Blu-ray drive with random-access recording capability.


### -field IMAPI_PROFILE_TYPE_BD_REWRITABLE

A rewritable Blu-ray drive.


### -field IMAPI_PROFILE_TYPE_HD_DVD_ROM

A read only high density DVD drive.


### -field IMAPI_PROFILE_TYPE_HD_DVD_RECORDABLE

A write once high density DVD drive.


### -field IMAPI_PROFILE_TYPE_HD_DVD_RAM

A high density DVD drive with random access positioning.


### -field IMAPI_PROFILE_TYPE_NON_STANDARD

Nonstandard drive.


## -remarks



Note that the range of feature type values is 0x0000 to 0xFFFF. This enumeration contains those features defined in the Multmedia Commands - 5 (MMC) specification. For a complete definition of each profile, see Profile Definitions in the latest release of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.

Other values not defined here may exist. Consumers of this enumeration should not presume this list to be the only set of valid values.




## -see-also




<a href="https://msdn.microsoft.com/7ee1b58b-0289-42e8-a23d-2600b9dd2e21">IDiscRecorder2::get_SupportedProfiles</a>



<a href="https://msdn.microsoft.com/1295d536-8531-4470-a8b4-1e589736e0b1">IDiscRecorder2Ex::GetSupportedProfiles</a>
 

 

