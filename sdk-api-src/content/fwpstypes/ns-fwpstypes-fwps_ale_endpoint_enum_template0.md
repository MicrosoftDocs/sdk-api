---
UID: NS:fwpstypes.FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_
title: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
author: windows-sdk-content
description: The FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure specifies a template for application layer enforcement (ALE) endpoints to be enumerated.Note  FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 is a specific version of FWPS_ALE_ENDPOINT_ENUM_TEMPLATE.
old-location: netvista\fwps_ale_endpoint_enum_template0.htm
tech.root: NetVista
ms.assetid: 7875bf42-4510-4af1-8f24-4b9f1d945100
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0, FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0, netvista.fwps_ale_endpoint_enum_template0, wfp_ref_3_struct_3_fwps_A-E_1d06d4d7-6e8f-4f8d-b57e-96292a680e68.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
req.redist: 
---

# FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure


## -description


The <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> structure specifies a template for application layer enforcement
  (ALE) endpoints to be enumerated.
<div class="alert"><b>Note</b>  <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> is a specific version of <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field localSubNet

The local subnet portion of the enumeration template.


### -field remoteSubNet

The remote subnet portion of the enumeration template.


### -field ipProtocol

The IP protocol portion of the enumeration template.


### -field localPort

The local port portion of the enumeration template.


### -field remotePort

The remote port portion of the enumeration template.


## -remarks



This structure can be used to narrow the results when enumerating endpoints. If used, it is specified
    when the enumeration handle is created by calling 
    <a href="https://msdn.microsoft.com/5daa3dd4-e499-4a72-b784-8a0e1ef3e92b">FwpsAleEndpointCreateEnumHandle0</a>. Any populated members are used to limit the enumeration results
    returned by 
    <a href="https://msdn.microsoft.com/8b3257ea-9eeb-426b-8c82-a4f0242861a8">FwpsAleEndpointEnum0</a>.




## -see-also




<a href="https://msdn.microsoft.com/5daa3dd4-e499-4a72-b784-8a0e1ef3e92b">FwpsAleEndpointCreateEnumHandle0</a>



<a href="https://msdn.microsoft.com/8b3257ea-9eeb-426b-8c82-a4f0242861a8">FwpsAleEndpointEnum0</a>
 

 

