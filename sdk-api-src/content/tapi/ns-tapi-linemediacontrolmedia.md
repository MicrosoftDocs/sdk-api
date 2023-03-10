---
UID: NS:tapi.linemediacontrolmedia_tag
title: LINEMEDIACONTROLMEDIA (tapi.h)
description: The LINEMEDIACONTROLMEDIA structure describes a media action to be executed when detecting a media type change. It is used as an entry in an array. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
helpviewer_keywords: ["*LPLINEMEDIACONTROLMEDIA","LINEMEDIACONTROLMEDIA","LINEMEDIACONTROLMEDIA structure [TAPI 2.2]","LPLINEMEDIACONTROLMEDIA","LPLINEMEDIACONTROLMEDIA structure pointer [TAPI 2.2]","_tapi2_linemediacontrolmedia_str","tapi/LINEMEDIACONTROLMEDIA","tapi/LPLINEMEDIACONTROLMEDIA","tapi2.linemediacontrolmedia_str"]
old-location: tapi2\linemediacontrolmedia_str.htm
tech.root: tapi3
ms.assetid: 5515d510-3827-4da6-975c-ff191bb0ab4e
ms.date: 12/05/2018
ms.keywords: '*LPLINEMEDIACONTROLMEDIA, LINEMEDIACONTROLMEDIA, LINEMEDIACONTROLMEDIA structure [TAPI 2.2], LPLINEMEDIACONTROLMEDIA, LPLINEMEDIACONTROLMEDIA structure pointer [TAPI 2.2], _tapi2_linemediacontrolmedia_str, tapi/LINEMEDIACONTROLMEDIA, tapi/LPLINEMEDIACONTROLMEDIA, tapi2.linemediacontrolmedia_str'
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
req.typenames: LINEMEDIACONTROLMEDIA, *LPLINEMEDIACONTROLMEDIA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linemediacontrolmedia_tag
 - tapi/linemediacontrolmedia_tag
 - LPLINEMEDIACONTROLMEDIA
 - tapi/LPLINEMEDIACONTROLMEDIA
 - LINEMEDIACONTROLMEDIA
 - tapi/LINEMEDIACONTROLMEDIA
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
 - LINEMEDIACONTROLMEDIA
---

# LINEMEDIACONTROLMEDIA structure


## -description

The 
<b>LINEMEDIACONTROLMEDIA</b> structure describes a media action to be executed when detecting a media type change. It is used as an entry in an array. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a> functions use this structure.

## -struct-fields

### -field dwMediaModes

One or more media types. This member uses one of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>.

### -field dwDuration

Duration of time during which the media type should be present before the application should be notified or media control action should be taken, in milliseconds.

### -field dwMediaControl

Media control action. This member uses one of the 
<a href="/windows/desktop/Tapi/linemediacontrol--constants">LINEMEDIACONTROL_ Constants</a>.

## -remarks

This structure may not be extended.

The 
<b>LINEMEDIACONTROLMEDIA</b> structure defines a triple &lt;media type(s), duration, media-control action&gt;. An array of these triples is passed to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> function to set the media control actions triggered by media type changes for a given call. When a change to a listed media type is detected, then the corresponding action on the media stream is invoked.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a>