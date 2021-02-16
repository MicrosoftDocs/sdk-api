---
UID: NS:tapi.linecalltreatmententry_tag
title: LINECALLTREATMENTENTRY (tapi.h)
description: The LINECALLTREATMENTENTRY structure provides information on the type of call treatment, such as music, recorded announcement, or silence, on the current call. The LINEADDRESSCAPS structure can contain an array of LINECALLTREATMENTENTRY structures.
helpviewer_keywords: ["*LPLINECALLTREATMENTENTRY","LINECALLTREATMENTENTRY","LINECALLTREATMENTENTRY structure [TAPI 2.2]","LPLINECALLTREATMENTENTRY","LPLINECALLTREATMENTENTRY structure pointer [TAPI 2.2]","_tapi2_linecalltreatmententry_str","tapi/LINECALLTREATMENTENTRY","tapi/LPLINECALLTREATMENTENTRY","tapi2.linecalltreatmententry_str"]
old-location: tapi2\linecalltreatmententry_str.htm
tech.root: tapi3
ms.assetid: c4a9fbb1-5201-45bd-b88c-b0c81b216f72
ms.date: 12/05/2018
ms.keywords: '*LPLINECALLTREATMENTENTRY, LINECALLTREATMENTENTRY, LINECALLTREATMENTENTRY structure [TAPI 2.2], LPLINECALLTREATMENTENTRY, LPLINECALLTREATMENTENTRY structure pointer [TAPI 2.2], _tapi2_linecalltreatmententry_str, tapi/LINECALLTREATMENTENTRY, tapi/LPLINECALLTREATMENTENTRY, tapi2.linecalltreatmententry_str'
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
targetos: Windows
req.typenames: LINECALLTREATMENTENTRY, *LPLINECALLTREATMENTENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecalltreatmententry_tag
 - tapi/linecalltreatmententry_tag
 - LPLINECALLTREATMENTENTRY
 - tapi/LPLINECALLTREATMENTENTRY
 - LINECALLTREATMENTENTRY
 - tapi/LINECALLTREATMENTENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINECALLTREATMENTENTRY
---

# LINECALLTREATMENTENTRY structure


## -description

The 
<b>LINECALLTREATMENTENTRY</b> structure provides information on the type of call treatment, such as music, recorded announcement, or silence, on the current call. The 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> structure can contain an array of 
<b>LINECALLTREATMENTENTRY</b> structures.

## -struct-fields

### -field dwCallTreatmentID

One of the 
<a href="/windows/desktop/Tapi/linecalltreatment--constants">LINECALLTREATMENT_ Constants</a> (if the treatment is of a predefined type) or a service provider-specific value.

### -field dwCallTreatmentNameSize

Size of the call treatment name string, in bytes, including the null-terminating character.

### -field dwCallTreatmentNameOffset

Offset from the beginning of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> to a null-terminated string identifying the treatment. This would ordinarily describe the content of the music or recorded announcement. If the treatment is of a predefined type, a meaningful name should still be specified, for example, "Silence\0", "Busy Signal\0", "Ringback\0", or "Music\0". The size of the string is specified by <b>dwCallTreatmentNameOffset</b>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/Tapi/linecalltreatment--constants">LINECALLTREATMENT_ Constants</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetcalltreatment">lineSetCallTreatment</a>