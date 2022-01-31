---
UID: NE:mediaobj._DMO_PROCESS_OUTPUT_FLAGS
title: "_DMO_PROCESS_OUTPUT_FLAGS (mediaobj.h)"
description: The DMO_PROCESS_OUTPUT_FLAGS enumeration defines flags that specify output processing requests.
helpviewer_keywords: ["DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","DMO_PROCESS_OUTPUT_FLAGS","DMO_PROCESS_OUTPUT_FLAGSEnumeration","_DMO_PROCESS_OUTPUT_FLAGS","_DMO_PROCESS_OUTPUT_FLAGS enumeration [DirectShow]","dshow.dmo_process_output_flags","mediaobj/DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","mediaobj/_DMO_PROCESS_OUTPUT_FLAGS"]
old-location: dshow\dmo_process_output_flags.htm
tech.root: dshow
ms.assetid: 7648f975-3753-41fe-a311-e86334ef7071
ms.date: 12/05/2018
ms.keywords: DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, DMO_PROCESS_OUTPUT_FLAGS , DMO_PROCESS_OUTPUT_FLAGSEnumeration, _DMO_PROCESS_OUTPUT_FLAGS, _DMO_PROCESS_OUTPUT_FLAGS enumeration [DirectShow], dshow.dmo_process_output_flags, mediaobj/DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, mediaobj/_DMO_PROCESS_OUTPUT_FLAGS
req.header: mediaobj.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_PROCESS_OUTPUT_FLAGS
 - mediaobj/_DMO_PROCESS_OUTPUT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_PROCESS_OUTPUT_FLAGS
---

# _DMO_PROCESS_OUTPUT_FLAGS enumeration


## -description

The <code>DMO_PROCESS_OUTPUT_FLAGS</code> enumeration defines flags that specify output processing requests.

## -enum-fields

### -field DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER:0x1

Discard the output when the pointer to the output buffer is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a>
