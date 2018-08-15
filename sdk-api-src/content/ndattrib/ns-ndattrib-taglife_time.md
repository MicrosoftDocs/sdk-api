---
UID: NS:ndattrib.tagLIFE_TIME
title: tagLIFE_TIME
author: windows-sdk-content
description: The LIFE_TIME structure contains a start time and an end time.
old-location: ndf\life_time.htm
old-project: ndf
ms.assetid: 31f038fb-08c1-4057-af61-f3912cfcd4f0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLIFE_TIME, LIFE_TIME, LIFE_TIME structure [NDF], LIFE_TIME,*PLIFE_TIME, LIFE_TIME,*PLIFE_TIME structure [NDF], ndattrib/LIFE_TIME, ndf.life_time, tagLIFE_TIME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ndattrib.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: LIFE_TIME, *PLIFE_TIME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - LIFE_TIME, *PLIFE_TIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagLIFE_TIME structure


## -description


The <b>LIFE_TIME</b> structure contains a start time and an end time.


## -struct-fields




### -field startTime

Type: <b>FILETIME</b>

The time the problem instance began.


### -field endTime

Type: <b>FILETIME</b>

The time the problem instance ended.

