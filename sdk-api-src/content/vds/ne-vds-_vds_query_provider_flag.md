---
UID: NE:vds._VDS_QUERY_PROVIDER_FLAG
title: "_VDS_QUERY_PROVIDER_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for provider query operations. Callers can query for hardware providers, software providers, or both.
old-location: base\vds_query_provider_flag.htm
old-project: vds
ms.assetid: 849b3cbc-a1ed-438a-8fda-ada096fb8375
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_QUERY_HARDWARE_PROVIDERS, VDS_QUERY_PROVIDER_FLAG, VDS_QUERY_PROVIDER_FLAG enumeration [VDS], VDS_QUERY_SOFTWARE_PROVIDERS, VDS_QUERY_VIRTUALDISK_PROVIDERS, _VDS_QUERY_PROVIDER_FLAG, base.vds_query_provider_flag, vds/VDS_QUERY_HARDWARE_PROVIDERS, vds/VDS_QUERY_PROVIDER_FLAG, vds/VDS_QUERY_SOFTWARE_PROVIDERS, vds/VDS_QUERY_VIRTUALDISK_PROVIDERS, vdshwprv/VDS_QUERY_HARDWARE_PROVIDERS, vdshwprv/VDS_QUERY_PROVIDER_FLAG, vdshwprv/VDS_QUERY_SOFTWARE_PROVIDERS, vdshwprv/VDS_QUERY_VIRTUALDISK_PROVIDERS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_QUERY_PROVIDER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_QUERY_PROVIDER_FLAG
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_QUERY_PROVIDER_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for provider query operations. Callers can query for hardware providers, software providers, or both.


## -enum-fields




### -field VDS_QUERY_SOFTWARE_PROVIDERS

If set, the operation queries for software providers.


### -field VDS_QUERY_HARDWARE_PROVIDERS

If set, the operation queries for hardware providers.


### -field VDS_QUERY_VIRTUALDISK_PROVIDERS

If set, the operation queries for virtual disk providers.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


## -remarks



This enumeration provides the value for the <i>masks</i> parameter of the  <a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">IVdsService::QueryProviders</a> method. You can specify more than  one value in the same query. For example, to query for software and hardware providers, specify both VDS_QUERY_SOFTWARE_PROVIDERS and VDS_QUERY_HARDWARE_PROVIDERS in the <i>masks</i> parameter.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_QUERY_PROVIDER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_QUERY_PROVIDER_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">IVdsService::QueryProviders</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

