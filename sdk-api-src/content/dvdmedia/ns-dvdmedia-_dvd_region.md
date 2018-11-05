---
UID: NS:dvdmedia._DVD_REGION
title: "_DVD_REGION"
author: windows-sdk-content
description: Identifies the DVD region as reported by the local system components.
old-location: dshow\dvd_region.htm
tech.root: DirectShow
ms.assetid: 2a555f98-5037-4a99-a1b7-bea36527309b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PDVD_REGION, DVD_REGION, DVD_REGION structure [DirectShow], DVD_REGIONStructure, PDVD_REGION, PDVD_REGION structure pointer [DirectShow], _DVD_REGION, dshow.dvd_region, dvdmedia/DVD_REGION, dvdmedia/PDVD_REGION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dvdmedia.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - DVD_REGION
product: Windows
targetos: Windows
req.typenames: DVD_REGION, *PDVD_REGION
req.redist: 
---

# _DVD_REGION structure


## -description



Identifies the DVD region as reported by the local system components.




## -struct-fields




### -field CopySystem

Specifies whether the disk is copy protected.


### -field RegionData

Contains information about the region from the decoder.


### -field SystemRegion

Contains information about region from DVD drive.


### -field ResetCount

 




#### - Reserved

Reserved.


## -remarks



The AM_PROPERTY_DVDCOPY_REGION property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/da3abefd-8f25-449d-8787-84d2cef928da">DVD Copy Protection Property Set</a>
 

 

