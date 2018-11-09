---
UID: NS:vds._VDS_PATH_INFO
title: "_VDS_PATH_INFO"
author: windows-sdk-content
description: Defines the information for a LUN path. This structure is returned in the ppPaths parameter of the IVdsLunMpio::GetPathInfo method.
old-location: base\vds_path_info.htm
tech.root: VDS
ms.assetid: 14444252-11ca-4614-81d1-9a15e76d0186
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDS_PATH_INFO, VDS_PATH_INFO structure, _VDS_PATH_INFO, base.vds_path_info, vds/VDS_PATH_INFO, vdshwprv/VDS_PATH_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - VDS_PATH_INFO
product: Windows
targetos: Windows
req.typenames: VDS_PATH_INFO
req.redist: VDS 1.1
---

# _VDS_PATH_INFO structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   information for a LUN path. This structure is returned in the <i>ppPaths</i> parameter of the <a href="https://msdn.microsoft.com/c7cc1abf-c7f2-4260-b9d2-f70128276e1e">IVdsLunMpio::GetPathInfo</a>  method.


## -struct-fields




### -field pathId

The unique ID of the path used by MPIO.


### -field type

The type of interconnect that the hardware provider supports for this LUN path. <a href="vds_hwprovider_type.htm">VDS_HWT_HYBRID</a> is not a valid value for this member, even if the provider is a hybrid provider.


### -field status

The status of the path, enumerated by 
      <a href="https://msdn.microsoft.com/f0682db1-9058-4514-abb2-c10b936d4f41">VDS_PATH_STATUS</a>.


### -field controllerPortId

The <b>VDS_OBJECT_ID</b> of the controller port object on the other end of the 
       path.


### -field targetPortalId

The <b>VDS_OBJECT_ID</b> of the target portal object on the other end of the 
       path.


### -field hbaPortId

The <b>VDS_OBJECT_ID</b> of the HBA port.


### -field initiatorAdapterId

The <b>VDS_OBJECT_ID</b> of the initiator adapter.


### -field pHbaPortProp

A pointer to a <a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a> structure 
       containing properties of the HBA port on one end of the path.


### -field pInitiatorPortalIpAddr

A pointer to a <a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a> structure containing 
       the IP address and port information for the initiator portal.


## -see-also




<a href="https://msdn.microsoft.com/c7cc1abf-c7f2-4260-b9d2-f70128276e1e">IVdsLunMpio::GetPathInfo</a>



<a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a>



<a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a>



<a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a>



<a href="https://msdn.microsoft.com/bfb786fc-eb03-4449-b631-fb85813c08c8">VDS_PATH_ID</a>



<a href="https://msdn.microsoft.com/f0682db1-9058-4514-abb2-c10b936d4f41">VDS_PATH_STATUS</a>
 

 

