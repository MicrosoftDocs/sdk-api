---
UID: NS:vds.VDS_REPARSE_POINT_PROP
title: VDS_REPARSE_POINT_PROP
author: windows-sdk-content
description: Defines the reparse-point properties of a volume object.
old-location: base\vds_reparse_point_prop.htm
old-project: vds
ms.assetid: 7e224f49-c51f-447e-bc0b-6af3843e01ae
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PVDS_REPARSE_POINT_PROP, PVDS_REPARSE_POINT_PROP, PVDS_REPARSE_POINT_PROP structure pointer [VDS], VDS_REPARSE_POINT_PROP, VDS_REPARSE_POINT_PROP structure [VDS], base.vds_reparse_point_prop, vds/PVDS_REPARSE_POINT_PROP, vds/VDS_REPARSE_POINT_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: VDS_REPARSE_POINT_PROP, *PVDS_REPARSE_POINT_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_REPARSE_POINT_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# VDS_REPARSE_POINT_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the reparse-point properties of a  <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a>.


## -struct-fields




### -field SourceVolumeId

The GUID of the volume object that contains the reparse point.


### -field pwszPath

A string for a path without a drive letter. For example, "\mount".


## -remarks



The <a href="https://msdn.microsoft.com/ae79355d-2012-42bf-930d-2915c4ca502c">IVdsVolumeMF::QueryReparsePoints</a>method returns this structure to report the reparse-point properties of a <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a>.




## -see-also




<a href="https://msdn.microsoft.com/ae79355d-2012-42bf-930d-2915c4ca502c">IVdsVolumeMF::QueryReparsePoints</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

