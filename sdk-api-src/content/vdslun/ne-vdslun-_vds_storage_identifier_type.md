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

# _VDS_STORAGE_IDENTIFIER_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a storage identifier.


## -enum-fields




### -field VDSStorageIdTypeVendorSpecific

The storage identifier type is vendor specific.


### -field VDSStorageIdTypeVendorId

The storage identifier is the same as the vendor identifier.


### -field VDSStorageIdTypeEUI64

The storage identifier type follows the IEEE 64-bit Extended Unique Identifier (EUI-64) standard.


### -field VDSStorageIdTypeFCPHName

The storage identifier type follows the Fibre Channel Physical and Signaling Interface (FC-PH) naming 
      convention.


### -field VDSStorageIdTypePortRelative

<b>VDS 1.1:  </b>The storage identifier type is dependent on the port.


### -field VDSStorageIdTypeTargetPortGroup


### -field VDSStorageIdTypeLogicalUnitGroup


### -field VDSStorageIdTypeMD5LogicalUnitIdentifier


### -field VDSStorageIdTypeScsiNameString




#### - VDSStorageIdTypeSCSINameString

<b>VDS 1.1:  </b>The storage identifier type follows the SCSI naming convention. See SCSI Primary Commands - 3 (SPC-3) for 
        more details.


## -remarks



The <a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a> structure 
    includes a <b>VDS_STORAGE_IDENTIFIER_TYPE</b> value as a member to indicate the storage identifier type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_IDENTIFIER_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_IDENTIFIER_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a>
 

 

