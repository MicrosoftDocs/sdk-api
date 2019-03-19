---
UID: NE:vds._VDS_STORAGE_POOL_STATUS
title: VDS_STORAGE_POOL_STATUS (vds.h)
author: windows-sdk-content
description: Defines the set of object status values for a storage pool.
old-location: base\vds_storage_pool_status.htm
tech.root: VDS
ms.assetid: b2af30c8-116c-4e51-bffc-0dee9a4bd04e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_SPS_NOT_READY, VDS_SPS_OFFLINE, VDS_SPS_ONLINE, VDS_SPS_UNKNOWN, VDS_STORAGE_POOL_STATUS, VDS_STORAGE_POOL_STATUS enumeration, base.vds_storage_pool_status, vds/VDS_SPS_NOT_READY, vds/VDS_SPS_OFFLINE, vds/VDS_SPS_ONLINE, vds/VDS_SPS_UNKNOWN, vds/VDS_STORAGE_POOL_STATUS, vdshwprv/VDS_SPS_NOT_READY, vdshwprv/VDS_SPS_OFFLINE, vdshwprv/VDS_SPS_ONLINE, vdshwprv/VDS_SPS_UNKNOWN, vdshwprv/VDS_STORAGE_POOL_STATUS
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_STORAGE_POOL_STATUS
product: Windows
targetos: Windows
req.typenames: VDS_STORAGE_POOL_STATUS
req.redist: 
---

# VDS_STORAGE_POOL_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.


## -enum-fields




### -field VDS_SPS_UNKNOWN

The provider failed to get the storage pool properties or could not access the storage pool.


### -field VDS_SPS_ONLINE

The storage pool is available.


### -field VDS_SPS_NOT_READY

The storage pool is busy.


### -field VDS_SPS_OFFLINE

The storage pool is not available.


## -remarks



The <a href="https://msdn.microsoft.com/2a82e872-2005-4b05-b67a-161b16c4f3aa">VDS_STORAGE_POOL_PROP</a> structure uses a <b>VDS_STORAGE_POOL_STATUS</b> value in the <a href="https://msdn.microsoft.com/en-us/library/Dd405631(v=VS.85).aspx">status</a> member to indicate the current status of the storage pool.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_POOL_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_POOL_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a82e872-2005-4b05-b67a-161b16c4f3aa">VDS_STORAGE_POOL_PROP</a>
 

 

