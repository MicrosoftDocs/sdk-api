---
UID: NS:mpeg2bits.MPEG_HEADER_VERSION_BITS
title: MPEG_HEADER_VERSION_BITS
author: windows-sdk-content
description: The MPEG_HEADER_VERSION_BITS structure contains the first 8 bits following the TSID in an MPEG-2 PSI section. These bits contain the version number and the current/next indicator.
old-location: mstv\mpeg_header_version_bits.htm
tech.root: MSTV
ms.assetid: d9a33ca6-2e35-4f7c-8621-ce30effeb687
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMPEG_HEADER_VERSION_BITS, MPEG_HEADER_VERSION_BITS, MPEG_HEADER_VERSION_BITS structure [Microsoft TV Technologies], MPEG_HEADER_VERSION_BITSStructure, PMPEG_HEADER_VERSION_BITS, PMPEG_HEADER_VERSION_BITS structure pointer [Microsoft TV Technologies], mpeg2bits/MPEG_HEADER_VERSION_BITS, mpeg2bits/PMPEG_HEADER_VERSION_BITS, mstv.mpeg_header_version_bits"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpeg2bits.h
req.include-header: Mpeg2Structs.h
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
 - Mpeg2Bits.h
api_name:
 - MPEG_HEADER_VERSION_BITS
product: Windows
targetos: Windows
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
req.redist: 
---

# MPEG_HEADER_VERSION_BITS structure


## -description



The <b>MPEG_HEADER_VERSION_BITS</b> structure contains the first 8 bits following the TSID in an MPEG-2 PSI section. These bits contain the version number and the current/next indicator.




## -struct-fields




### -field CurrentNextIndicator

The current_next_indicator field.


### -field VersionNumber

The version_number field.


### -field Reserved

Two reserved bits.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

