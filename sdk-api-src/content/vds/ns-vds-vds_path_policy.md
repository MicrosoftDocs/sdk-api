---
UID: NS:vds._VDS_PATH_POLICY
title: VDS_PATH_POLICY
author: windows-sdk-content
description: Defines the load balance policy as it applies to a particular path.
old-location: base\vds_path_policy.htm
tech.root: vds
ms.assetid: 7dec1d91-6781-42fa-9476-bb64e2554017
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_PATH_POLICY, VDS_PATH_POLICY structure [VDS], base.vds_path_policy, vds/VDS_PATH_POLICY, vdshwprv/VDS_PATH_POLICY
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - VDS_PATH_POLICY
product: Windows
targetos: Windows
req.typenames: VDS_PATH_POLICY
req.redist: 
---

# VDS_PATH_POLICY structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
    load balance policy as it applies to a particular path.


## -struct-fields




### -field pathId

The ID of the path used by MPIO.


### -field bPrimaryPath

If set, indicates that the path is a primary path for MPIO.


### -field ulWeight

The weight assigned to the path. This is only relevant if the load balance policy for the LUN is 
      <b>VDS_LBP_WEIGHTED_PATHS</b>.


## -see-also




<a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/2f3eb00a-864e-4fb7-a722-4537e6b8dd42">IVdsLunMpio::SetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

