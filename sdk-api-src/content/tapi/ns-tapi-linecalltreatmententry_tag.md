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

# linecalltreatmententry_tag structure


## -description


The 
<b>LINECALLTREATMENTENTRY</b> structure provides information on the type of call treatment, such as music, recorded announcement, or silence, on the current call. The 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> structure can contain an array of 
<b>LINECALLTREATMENTENTRY</b> structures.


## -struct-fields




### -field dwCallTreatmentID

One of the 
<a href="https://msdn.microsoft.com/c28c9200-dd51-48b2-905c-fbe37c83b00f">LINECALLTREATMENT_ Constants</a> (if the treatment is of a predefined type) or a service provider-specific value.


### -field dwCallTreatmentNameSize

Size of the call treatment name string, in bytes, including the null-terminating character.


### -field dwCallTreatmentNameOffset

Offset from the beginning of 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> to a null-terminated string identifying the treatment. This would ordinarily describe the content of the music or recorded announcement. If the treatment is of a predefined type, a meaningful name should still be specified, for example, "Silence\0", "Busy Signal\0", "Ringback\0", or "Music\0". The size of the string is specified by <b>dwCallTreatmentNameOffset</b>.


## -see-also




<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/c28c9200-dd51-48b2-905c-fbe37c83b00f">LINECALLTREATMENT_ Constants</a>



<a href="https://msdn.microsoft.com/08cdea8a-5b36-428c-b90f-8741ae5f3205">lineGetAddressCaps</a>



<a href="https://msdn.microsoft.com/0f1a3303-f6c3-4a5f-99bd-35e107c9b0b0">lineSetCallTreatment</a>
 

 

