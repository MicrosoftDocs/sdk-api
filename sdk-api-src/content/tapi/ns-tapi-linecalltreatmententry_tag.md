---
UID: NS:tapi.linecalltreatmententry_tag
title: linecalltreatmententry_tag
author: windows-sdk-content
description: The LINECALLTREATMENTENTRY structure provides information on the type of call treatment, such as music, recorded announcement, or silence, on the current call. The LINEADDRESSCAPS structure can contain an array of LINECALLTREATMENTENTRY structures.
old-location: tapi2\linecalltreatmententry_str.htm
tech.root: tapi
ms.assetid: c4a9fbb1-5201-45bd-b88c-b0c81b216f72
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPLINECALLTREATMENTENTRY, LINECALLTREATMENTENTRY, LINECALLTREATMENTENTRY structure [TAPI 2.2], LPLINECALLTREATMENTENTRY, LPLINECALLTREATMENTENTRY structure pointer [TAPI 2.2], _tapi2_linecalltreatmententry_str, linecalltreatmententry_tag, tapi/LINECALLTREATMENTENTRY, tapi/LPLINECALLTREATMENTENTRY, tapi2.linecalltreatmententry_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tapi.h
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
 - Tapi.h
api_name:
 - LINECALLTREATMENTENTRY
product: Windows
targetos: Windows
req.typenames: LINECALLTREATMENTENTRY, *LPLINECALLTREATMENTENTRY
req.redist: 
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
 

 

