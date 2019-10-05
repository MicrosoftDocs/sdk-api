---
UID: NS:ndattrib.tagLIFE_TIME
title: LIFE_TIME (ndattrib.h)
author: windows-sdk-content
description: The LIFE_TIME structure contains a start time and an end time.
old-location: ndf\life_time.htm
tech.root: NDF
ms.assetid: 31f038fb-08c1-4057-af61-f3912cfcd4f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLIFE_TIME, LIFE_TIME, LIFE_TIME structure [NDF], LIFE_TIME,*PLIFE_TIME, LIFE_TIME,*PLIFE_TIME structure [NDF], ndattrib/LIFE_TIME, ndf.life_time"
ms.topic: struct
f1_keywords: 
 - "ndattrib/LIFE_TIME, *PLIFE_TIME"
dev_langs:
 - c++
req.header: ndattrib.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - LIFE_TIME, *PLIFE_TIME
targetos: Windows
req.typenames: LIFE_TIME, *PLIFE_TIME
req.redist: 
ms.custom: 19H1
---

# LIFE_TIME structure


## -description


The <b>LIFE_TIME</b> structure contains a start time and an end time.


## -struct-fields




### -field startTime

Type: <b>FILETIME</b>

The time the problem instance began.


### -field endTime

Type: <b>FILETIME</b>

The time the problem instance ended.

