---
UID: NS:vdslun._VDS_INTERCONNECT
title: "_VDS_INTERCONNECT"
author: windows-driver-content
description: Defines the address data of a physical interconnect.
old-location: base\vds_interconnect.htm
old-project: VDS
ms.assetid: fc9f532b-a37f-4338-95db-6ec988131211
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: VDS_INTERCONNECT, VDS_INTERCONNECT structure [VDS], _VDS_INTERCONNECT, base.vds_interconnect, vdslun/_VDS_INTERCONNECT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
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
req.typenames: VDS_INTERCONNECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VdsLun.h
api_name:
-	VDS_INTERCONNECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_INTERCONNECT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the address 
   data of a physical interconnect.


## -struct-fields




### -field m_addressType


      The interconnect address type enumerated by 
      <a href="https://msdn.microsoft.com/20d75585-a80c-49bc-9f9c-5aae8e5f2c21">VDS_INTERCONNECT_ADDRESS_TYPE</a>.


### -field m_cbPort

The size of the interconnect address data for the LUN port (<b>m_pbPort</b>), in bytes.


### -field m_pbPort

Pointer to the interconnect address data for the LUN port.


### -field m_cbAddress


      The size of the interconnect address data for the LUN (<b>m_pbAddress</b>), in bytes.


### -field m_pbAddress

Pointer to the interconnect address data for the LUN.


## -remarks




    The <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure includes this 
    structure as a member to specify an interconnect by which a LUN can be accessed.




## -see-also




<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/20d75585-a80c-49bc-9f9c-5aae8e5f2c21">VDS_INTERCONNECT_ADDRESS_TYPE</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>
 

 

