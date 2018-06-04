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

# _IMAPI_FEATURE_PAGE_TYPE enumeration


## -description


Defines values for the feature that are supported by the logical unit (CD and DVD device).  


## -enum-fields




### -field IMAPI_FEATURE_PAGE_TYPE_PROFILE_LIST

 Identifies profiles supported by the logical unit.


### -field IMAPI_FEATURE_PAGE_TYPE_CORE

 Identifies a logical unit that supports functionality common to all devices.


### -field IMAPI_FEATURE_PAGE_TYPE_MORPHING

Identifies the ability of the logical unit to notify an initiator about operational changes 
and accept initiator requests to prevent operational changes.


### -field IMAPI_FEATURE_PAGE_TYPE_REMOVABLE_MEDIUM

Identifies a logical unit that has a medium that is removable.


### -field IMAPI_FEATURE_PAGE_TYPE_WRITE_PROTECT

 Identifies reporting capability and changing capability for write protection status of the 
logical unit.


### -field IMAPI_FEATURE_PAGE_TYPE_RANDOMLY_READABLE

 Identifies a logical unit that is able to read data from logical blocks specified by Logical 
Block Addresses.


### -field IMAPI_FEATURE_PAGE_TYPE_CD_MULTIREAD

Identifies a logical unit that conforms to the OSTA Multi-Read specification 1.00, with the exception of CD 
Play capability (the CD Audio Feature is not required).


### -field IMAPI_FEATURE_PAGE_TYPE_CD_READ

 Identifies a logical unit that is able to read CD specific information from the media and 
is able to read user data from all types of CD blocks.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_READ

 Identifies a logical unit that is able to read DVD specific information from the media.


### -field IMAPI_FEATURE_PAGE_TYPE_RANDOMLY_WRITABLE

Identifies a logical unit that is able to write data to logical blocks specified by Logical 
Block Addresses. 


### -field IMAPI_FEATURE_PAGE_TYPE_INCREMENTAL_STREAMING_WRITABLE

 Identifies a logical unit that is able to write data to a contiguous region, and is able to 
append data to a limited number of locations on the media.


### -field IMAPI_FEATURE_PAGE_TYPE_SECTOR_ERASABLE

 Identifies a logical unit that supports erasable media and media that requires an erase 
pass before overwrite, such as some magneto-optical technologies.


### -field IMAPI_FEATURE_PAGE_TYPE_FORMATTABLE

 Identifies a logical unit that can format media into logical blocks.


### -field IMAPI_FEATURE_PAGE_TYPE_HARDWARE_DEFECT_MANAGEMENT

Identifies a logical unit that has defect management available to provide a 
defect-free contiguous address space.


### -field IMAPI_FEATURE_PAGE_TYPE_WRITE_ONCE

Identifies a logical unit that has the ability to record to any previously unrecorded 
logical block.


### -field IMAPI_FEATURE_PAGE_TYPE_RESTRICTED_OVERWRITE

 Identifies a logical unit that has the ability to overwrite logical blocks only in fixed 
sets at a time. 


### -field IMAPI_FEATURE_PAGE_TYPE_CDRW_CAV_WRITE

Identifies a logical unit that has the ability to write CD-RW media that is designed for 
CAV recording. 


### -field IMAPI_FEATURE_PAGE_TYPE_MRW

 Indicates that the logical unit is capable of reading a disc with the 
MRW format.


### -field IMAPI_FEATURE_PAGE_TYPE_ENHANCED_DEFECT_REPORTING

 Identifies a logical unit that has the ability to perform media 
certification and recovered error reporting for logical unit assisted software defect 
management.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_PLUS_RW

 Indicates that the logical unit is capable of reading a 
recorded DVD+RW disc.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_PLUS_R

 Indicates that the logical unit is capable of reading a recorded 
DVD+R disc.


### -field IMAPI_FEATURE_PAGE_TYPE_RIGID_RESTRICTED_OVERWRITE

Identifies a logical unit that has the ability to perform writing only on Blocking 
boundaries. 


### -field IMAPI_FEATURE_PAGE_TYPE_CD_TRACK_AT_ONCE

Identifies a logical unit that is able to write data to a CD track.


### -field IMAPI_FEATURE_PAGE_TYPE_CD_MASTERING

Identifies a logical unit that is able to write a CD in Session at Once mode or Raw mode.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE

 Identifies a logical unit that has the ability to write data to DVD-R/-RW in Disc at Once 
mode. 


### -field IMAPI_FEATURE_PAGE_TYPE_DOUBLE_DENSITY_CD_READ

Identifies a logical unit that has the ability to read double density CD specific information from the media.

<div class="alert"><b>Note</b>  This value has been deprecated.</div>
<div> </div>

### -field IMAPI_FEATURE_PAGE_TYPE_DOUBLE_DENSITY_CD_R_WRITE

Identifies a logical unit that has the ability to write to double density CD  media.

<div class="alert"><b>Note</b>  This value has been deprecated.</div>
<div> </div>

### -field IMAPI_FEATURE_PAGE_TYPE_DOUBLE_DENSITY_CD_RW_WRITE

Identifies a logical unit that has the ability to write to double density CD-RW  media.

<div class="alert"><b>Note</b>  This value has been deprecated.</div>
<div> </div>

### -field IMAPI_FEATURE_PAGE_TYPE_LAYER_JUMP_RECORDING

Identifies a drive that is able to write data to contiguous regions that are allocated on multiple
layers, and is able to append data to a limited number of locations on the media.


### -field IMAPI_FEATURE_PAGE_TYPE_CD_RW_MEDIA_WRITE_SUPPORT

 Identifies a logical unit that has the ability to perform writing CD-RW media.


### -field IMAPI_FEATURE_PAGE_TYPE_BD_PSEUDO_OVERWRITE

Identifies a drive that provides Logical Block overwrite service on BD-R discs that are
formatted as SRM+POW.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_PLUS_R_DUAL_LAYER

 Indicates that the drive is capable of reading a 
recorded DVD+R Double Layer disc


### -field IMAPI_FEATURE_PAGE_TYPE_BD_READ

Identifies a logical unit that is able to read control structures and user data from the Blu-ray 
disc. 


### -field IMAPI_FEATURE_PAGE_TYPE_BD_WRITE

Identifies a drive that is able to write control structures and user data to writeable Blu-ray discs.


### -field IMAPI_FEATURE_PAGE_TYPE_HD_DVD_READ

Identifies a drive that is able to read HD DVD specific information from the media.


### -field IMAPI_FEATURE_PAGE_TYPE_HD_DVD_WRITE

Indicates the ability to write to HD DVD-R/-RW media.


### -field IMAPI_FEATURE_PAGE_TYPE_POWER_MANAGEMENT

 Identifies a logical unit that is able to perform initiator and logical unit directed power 
management.


### -field IMAPI_FEATURE_PAGE_TYPE_SMART

Identifies a logical unit that is able to perform Self-Monitoring Analysis and Reporting 
Technology (S.M.A.R.T.). 


### -field IMAPI_FEATURE_PAGE_TYPE_EMBEDDED_CHANGER

 Identifies a logical unit that is able to move media from a storage area to a mechanism 
and back.


### -field IMAPI_FEATURE_PAGE_TYPE_CD_ANALOG_PLAY

 Identifies a logical unit that is able to play CD Audio data directly to an external output.


### -field IMAPI_FEATURE_PAGE_TYPE_MICROCODE_UPDATE

Identifies a logical unit that is able to upgrade its internal microcode via the interface.


### -field IMAPI_FEATURE_PAGE_TYPE_TIMEOUT

 Identifies a logical unit that is able to always respond to commands within a set time 
period.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_CSS

Identifies a logical unit that is able to perform DVD CSS/CPPM authentication and key 
management. This feature also indicates that the logical unit supports CSS for DVD-Video and CPPM for 
DVD-Audio. 


### -field IMAPI_FEATURE_PAGE_TYPE_REAL_TIME_STREAMING

Identifies a logical unit that is able to perform reading and writing within initiator 
specified (and logical unit verified) performance ranges.  This Feature also indicates whether the 
logical unit supports the stream playback operation.


### -field IMAPI_FEATURE_PAGE_TYPE_LOGICAL_UNIT_SERIAL_NUMBER

 Identifies a logical unit that has a unique serial number.


### -field IMAPI_FEATURE_PAGE_TYPE_MEDIA_SERIAL_NUMBER

Identifies a logical unit that is capable of reading a media serial number of the currently 
installed media.


### -field IMAPI_FEATURE_PAGE_TYPE_DISC_CONTROL_BLOCKS

 Identifies a logical unit that is able to read and/or write Disc Control Blocks from or to 
the media.


### -field IMAPI_FEATURE_PAGE_TYPE_DVD_CPRM

 Identifies a logical unit that is able to perform DVD CPRM and is able to perform CPRM 
authentication and key management.


### -field IMAPI_FEATURE_PAGE_TYPE_FIRMWARE_INFORMATION

 Indicates that the logical unit provides the date and time of the creation of the 
current firmware revision loaded on the device. 


### -field IMAPI_FEATURE_PAGE_TYPE_AACS

Identifies a drive that supports AACS and is able to perform AACS authentication process.


### -field IMAPI_FEATURE_PAGE_TYPE_VCPS

Identifies a Drive that is able to process disc data structures that are specified in the
VCPS.


## -remarks



Note that the range of feature type values is 0x0000 to 0xFFFF. This enumeration contains those features defined in the Multmedia Commands - 5 (MMC) specification. For a complete definition of each feature, see Feature Definitions in the latest release of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.

Other values not defined here may exist. Consumers of this enumeration should not presume this list to be the only set of valid values.




## -see-also




<a href="https://msdn.microsoft.com/e2764de1-85cc-4f04-951d-5cb70575ee9f">IDiscRecorder2::get_SupportedFeaturePages</a>



<a href="https://msdn.microsoft.com/a3cf0d33-25ea-4764-8fdb-5ef47c7b1e50">IDiscRecorder2Ex::GetFeaturePage</a>



<a href="https://msdn.microsoft.com/64fa8ef5-1298-4fd1-b89d-371f13e50d8c">IDiscRecorder2Ex::GetSupportedFeaturePages</a>
 

 

