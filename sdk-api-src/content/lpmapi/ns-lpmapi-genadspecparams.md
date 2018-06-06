---
UID: NS:lpmapi.GenAdspecParams
title: GenAdspecParams
author: windows-sdk-content
description: The GenAdspecParams structure contains general path characterization parameters.
old-location: qos\genadspecparams.htm
old-project: QOS
ms.assetid: 0d980286-bce6-483e-b2a1-117c7280c1c1
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GenAdspecParams, GenAdspecParams structure [QOS], lpmapi/GenAdspecParams, qos.genadspecparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: GenAdspecParams
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GenAdspecParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# GenAdspecParams structure


## -description


The 
<b>GenAdspecParams</b> structure contains general path characterization parameters.


## -struct-fields




### -field gen_parm_hdr

General information and length information for the Adspec parameters object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field gen_parm_hopcnt_hdr

Parameter header for hop count information associated with the Adspec object, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field gen_parm_hopcnt

Hop count information parameter.


### -field gen_parm_pathbw_hdr

Parameter header for path bandwidth information associated with the Adspec object, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field gen_parm_path_bw

Path bandwidth information parameter.


### -field gen_parm_minlat_hdr

Parameter header for minimum latency information associated with the Adspec object, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field gen_parm_min_latency

Minimum latency information parameter.


### -field gen_parm_compmtu_hdr

Parameter header for composed maximum transmission unit (MTU) information associated with the Adspec object, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field gen_parm_composed_MTU

Composed MTU information parameter.


## -see-also




<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>
 

 

