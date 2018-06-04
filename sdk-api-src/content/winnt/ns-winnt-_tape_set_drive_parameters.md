---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _TAPE_SET_DRIVE_PARAMETERS structure


## -description


The 
<b>TAPE_SET_DRIVE_PARAMETERS</b> structure describes the tape drive. It is used by the <a href="https://msdn.microsoft.com/2043249b-b4ff-4bdd-9e6e-13c432a183cb">SetTapeParameters</a>
		function.


## -struct-fields




### -field ECC

If this member is <b>TRUE</b>, hardware error correction is supported. Otherwise, it is not.


### -field Compression

If this member is <b>TRUE</b>, hardware data compression is enabled. Otherwise, it is disabled.


### -field DataPadding

If this member is <b>TRUE</b>, data padding is enabled. Otherwise, it is disabled. Data padding keeps the tape streaming at a constant speed.


### -field ReportSetmarks

If this member is <b>TRUE</b>, setmark reporting is enabled. Otherwise, it is disabled.


### -field EOTWarningZoneSize

Number of bytes between the end-of-tape warning and the physical end of the tape.


## -see-also




<a href="https://msdn.microsoft.com/2043249b-b4ff-4bdd-9e6e-13c432a183cb">SetTapeParameters</a>
 

 

