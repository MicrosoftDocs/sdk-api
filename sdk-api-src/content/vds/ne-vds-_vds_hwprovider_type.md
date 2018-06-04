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

# _VDS_HWPROVIDER_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a hardware provider.  These values are used in the 
  <b>type</b> member of the <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> 
  structure and are returned in the <i>pType</i> parameter of the <a href="https://msdn.microsoft.com/e88fd2df-531d-46d8-a91b-9b9f8578e57b">IVdsHwProviderType::GetProviderType</a> method.


## -enum-fields




### -field VDS_HWT_UNKNOWN

The type is unknown.


### -field VDS_HWT_PCI_RAID

The type indicates a hardware provider for PCI RAID cards.


### -field VDS_HWT_FIBRE_CHANNEL

The type indicates a hardware provider for Fibre Channel storage array networks.


### -field VDS_HWT_ISCSI

The type indicates a hardware provider for iSCSI storage array networks.


### -field VDS_HWT_SAS

The type indicates a hardware provider for serial attached SCSI (SAS) storage array networks.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7.


### -field VDS_HWT_HYBRID

The type indicates a hybrid hardware provider. A hybrid provider is a provider that manages subsystems that support multiple interconnect types. This is not a valid value for the  
  <b>type</b> member of the <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> 
  structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7.


## -remarks



If your application encounters a <b>VDS_HWPROVIDER_TYPE</b> value that it does not recognize, it should display the provider type as unknown. It should not attempt to map the unrecognized provider type to another provider type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HWPROVIDER_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HWPROVIDER_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e88fd2df-531d-46d8-a91b-9b9f8578e57b">IVdsHwProviderType::GetProviderType</a>



<a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">IVdsService::QueryProviders</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a>
 

 

