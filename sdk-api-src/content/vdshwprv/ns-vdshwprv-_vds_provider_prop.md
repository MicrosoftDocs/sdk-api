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

# _VDS_PROVIDER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="https://msdn.microsoft.com/131e927d-d32a-44f6-8aae-28839cfa9e7d">provider object</a>.


## -struct-fields




### -field id

The GUID of the provider object.


### -field pwszName

A string representing the name of the provider.


### -field guidVersionId

The version-specific GUID of the provider.


### -field pwszVersion

A string representing the version of the provider.


### -field type

The provider types enumerated by 
      <a href="https://msdn.microsoft.com/a794e054-1389-4b54-9ad3-eb32b9dd0a5b">VDS_PROVIDER_TYPE</a>.


### -field ulFlags

The provider flags enumerated by 
      <a href="https://msdn.microsoft.com/610e11a8-6670-4e76-baa6-58dd78f7611b">VDS_PROVIDER_FLAG</a>.


### -field ulStripeSizeFlags

The size of a stripe to be used across multiple disks managed by a software provider. A stripe size must be 
      a power of 2. Each bit in the 32-bit integer represents a size, in bytes. For example, if the <i>n</i>th bit is set, then 
      VDS supports stripe size of 2^<i>n</i>. Thus, bits 0 through 31 can specify 2^0 through 2^31.

The basic provider sets this value to zero. The dynamic stripe size can be any power of 2 ranging from 512 
      to 1MB.
     

<b>Windows Server 2003:  </b>The dynamic provider sets this value to 64k.


### -field sRebuildPriority

The rebuild priority used by software providers to specify the regeneration order when a mirrored or 
      striped with parity (RAID-5) volume requires rebuilding. Priority levels are 0 (lowest priority) to 15 (highest priority). VDS propagates the 
      priority to all new volumes created by the provider. Thus, all volumes managed by a provider have the same 
      rebuild priority.

This member does not apply to the basic provider and is zero for the dynamic provider.


## -remarks



The <a href="https://msdn.microsoft.com/a4cb18c5-2cda-4d0a-9be0-4a548ec2f6eb">IVdsProvider::GetProperties</a> method 
    returns this structure to report the property details of a provider object.




## -see-also




<a href="https://msdn.microsoft.com/a4cb18c5-2cda-4d0a-9be0-4a548ec2f6eb">IVdsProvider::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/610e11a8-6670-4e76-baa6-58dd78f7611b">VDS_PROVIDER_FLAG</a>



<a href="https://msdn.microsoft.com/a794e054-1389-4b54-9ad3-eb32b9dd0a5b">VDS_PROVIDER_TYPE</a>
 

 

