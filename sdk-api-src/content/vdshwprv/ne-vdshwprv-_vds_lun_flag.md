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

# _VDS_LUN_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a LUN object.


## -enum-fields




### -field VDS_LF_LBN_REMAP_ENABLED

The provider remaps LUN extents to drive extents automatically.


### -field VDS_LF_READ_BACK_VERIFY_ENABLED

The provider verifies writes by readback.


### -field VDS_LF_WRITE_THROUGH_CACHING_ENABLED

The provider enables write-through caching on the LUN.


### -field VDS_LF_HARDWARE_CHECKSUM_ENABLED

The provider verifies the integrity of the read and write data using a checksum.


### -field VDS_LF_READ_CACHE_ENABLED

Read caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_WRITE_CACHE_ENABLED

Write caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_MEDIA_SCAN_ENABLED

Media scanning is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_CONSISTENCY_CHECK_ENABLED

Consistency checking is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_SNAPSHOT

The LUN is a volume shadow copy LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks




        This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a> structure and provides the value for the <b>VDS_LPF_LBN_REMAP_ENABLED</b> enumerator in the <a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a> enumeration.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a>
 

 

