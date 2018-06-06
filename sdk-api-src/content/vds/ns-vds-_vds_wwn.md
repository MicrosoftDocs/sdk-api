---
UID: NS:vds._VDS_WWN
title: "_VDS_WWN"
author: windows-sdk-content
description: Defines a world-wide name (WWN). This structure corresponds to the HBA_WWN structure defined by the ANSI HBA API.
old-location: base\vds_wwn.htm
old-project: VDS
ms.assetid: a6d546bd-26ba-4f49-aeed-1f5462cc0bab
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_WWN, VDS_WWN structure [VDS], _VDS_WWN, base.vds_wwn, vds/VDS_WWN, vdshwprv/VDS_WWN
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
tech.root: 
req.typenames: VDS_WWN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_WWN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_WWN structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a world-wide name (WWN). This 
   structure corresponds to the HBA_WWN structure defined by the ANSI HBA API.


## -struct-fields




### -field rguchWwn

An array of 8 bytes that together specify the 64-bit WWN value. The first element of the array is the most 
      significant byte of the WWN, with the most significant bit of that byte being the most significant bit of the 
      WWN.


## -see-also




<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a>
 

 

