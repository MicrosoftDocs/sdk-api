---
UID: NS:tapi.linemediacontroltone_tag
title: linemediacontroltone_tag
author: windows-sdk-content
description: The LINEMEDIACONTROLTONE structure describes a media action to be executed when a tone has been detected. It is used as an entry in an array. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
old-location: tapi2\linemediacontroltone_str.htm
old-project: tapi
ms.assetid: 0513d580-aaf1-412c-adbf-9342b74025ee
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "*LPLINEMEDIACONTROLTONE, LINEMEDIACONTROLTONE, LINEMEDIACONTROLTONE structure [TAPI 2.2], LPLINEMEDIACONTROLTONE, LPLINEMEDIACONTROLTONE structure pointer [TAPI 2.2], _tapi2_linemediacontroltone_str, linemediacontroltone_tag, tapi/LINEMEDIACONTROLTONE, tapi/LPLINEMEDIACONTROLTONE, tapi2.linemediacontroltone_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LINEMEDIACONTROLTONE, *LPLINEMEDIACONTROLTONE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMEDIACONTROLTONE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linemediacontroltone_tag structure


## -description


The 
<b>LINEMEDIACONTROLTONE</b> structure describes a media action to be executed when a tone has been detected. It is used as an entry in an array. The 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> and 
<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a> functions use this structure.


## -struct-fields




### -field dwAppSpecific

Used by the application for tagging the tone. When this tone is detected, the value of the <b>dwAppSpecific</b> member is passed back to the application.


### -field dwDuration

Duration of time during which the tone should be present before a detection is made, in milliseconds.


### -field dwFrequency1

First frequency of the tone, in hertz.


### -field dwFrequency2

Second frequency of the tone, in hertz.


### -field dwFrequency3

Third frequency of the tone, in hertz. If fewer than three frequencies are needed in the tone, a value of 0 should be used for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be use for silence detection.


### -field dwMediaControl

Media control action. This member uses one of the 
<a href="https://msdn.microsoft.com/1e8aeda8-2810-462a-bfba-0296d854d9aa">LINEMEDIACONTROL_ Constants</a>.


## -remarks



This structure may not be extended.

The 
<b>LINEMEDIACONTROLTONE</b> structure defines a tuple &lt;tone, media-control action&gt;. An array of these tuples is passed to the 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> function to set media control actions triggered by media type changes for a given call. When a change to a listed media type is detected, the corresponding action on the media stream is invoked.

A tone with all frequencies set to zero corresponds to silence. An application can thus monitor the call's information stream for silence.




## -see-also




<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a>



<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a>
 

 

