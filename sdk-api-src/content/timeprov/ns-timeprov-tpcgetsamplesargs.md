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

# TpcGetSamplesArgs structure


## -description


A structure that is used by the 
<a href="https://msdn.microsoft.com/07b0bdf2-d224-4bbc-be29-9032a848d5ae">TimeProvCommand</a> function.


## -struct-fields




### -field pbSampleBuf

An array of 
<a href="https://msdn.microsoft.com/020a6502-3357-4800-8fc4-0d73ae42aa51">TimeSample</a> structures.


### -field cbSampleBuf

The size of <b>pbSampleBuf</b>, in bytes.


### -field dwSamplesReturned

The number of samples returned.


### -field dwSamplesAvailable

The total number of samples available.


## -see-also




<a href="https://msdn.microsoft.com/07b0bdf2-d224-4bbc-be29-9032a848d5ae">TimeProvCommand</a>



<a href="https://msdn.microsoft.com/020a6502-3357-4800-8fc4-0d73ae42aa51">TimeSample</a>
 

 

