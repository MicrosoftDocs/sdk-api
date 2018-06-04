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

# ProtType enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>ProtType</b> enumeration type specifies various types of content protection.


## -enum-fields




### -field PROT_COPY_FREE

Copy Free.


### -field PROT_COPY_ONCE

Copy Once.


### -field PROT_COPY_NEVER

Copy Never.


### -field PROT_COPY_NEVER_REALLY

Reserved.


### -field PROT_COPY_NO_MORE

Copy No More.


### -field PROT_COPY_FREE_CIT

The Copy Control Information (CCI) flag indicates Copy Free, but the Constrained Image Trigger (CIT) bit is set. The content is encrypted.


### -field PROT_COPY_BF

Reserved.


### -field PROT_COPY_CN_RECORDING_STOP

Reserved.


### -field PROT_COPY_FREE_SECURE

The Copy Control Information (CCI) flag indicates Copy Free, but the Redistribution Control Trigger (RCT) bit is set. The content is encrypted.


### -field PROT_COPY_INVALID

Error or invalid protection scheme. Treat as Copy Never.


## -see-also




<a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a>



<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

