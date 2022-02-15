---
UID: NE:mediaobj._DMO_INPUT_DATA_BUFFER_FLAGS
title: "_DMO_INPUT_DATA_BUFFER_FLAGS (mediaobj.h)"
description: The DMO_INPUT_DATA_BUFFER_FLAGS enumeration defines flags that describe an input buffer.
helpviewer_keywords: ["DMO_INPUT_DATA_BUFFERF_SYNCPOINT","DMO_INPUT_DATA_BUFFERF_TIME","DMO_INPUT_DATA_BUFFERF_TIMELENGTH","DMO_INPUT_DATA_BUFFER_FLAGS","DMO_INPUT_DATA_BUFFER_FLAGSEnumeration","_DMO_INPUT_DATA_BUFFER_FLAGS","_DMO_INPUT_DATA_BUFFER_FLAGS enumeration [DirectShow]","dshow.dmo_input_data_buffer_flags","mediaobj/DMO_INPUT_DATA_BUFFERF_SYNCPOINT","mediaobj/DMO_INPUT_DATA_BUFFERF_TIME","mediaobj/DMO_INPUT_DATA_BUFFERF_TIMELENGTH","mediaobj/_DMO_INPUT_DATA_BUFFER_FLAGS"]
old-location: dshow\dmo_input_data_buffer_flags.htm
tech.root: dshow
ms.assetid: b0217926-ac2d-48e5-a5d0-e31be6ea20ac
ms.date: 12/05/2018
ms.keywords: DMO_INPUT_DATA_BUFFERF_SYNCPOINT, DMO_INPUT_DATA_BUFFERF_TIME, DMO_INPUT_DATA_BUFFERF_TIMELENGTH, DMO_INPUT_DATA_BUFFER_FLAGS , DMO_INPUT_DATA_BUFFER_FLAGSEnumeration, _DMO_INPUT_DATA_BUFFER_FLAGS, _DMO_INPUT_DATA_BUFFER_FLAGS enumeration [DirectShow], dshow.dmo_input_data_buffer_flags, mediaobj/DMO_INPUT_DATA_BUFFERF_SYNCPOINT, mediaobj/DMO_INPUT_DATA_BUFFERF_TIME, mediaobj/DMO_INPUT_DATA_BUFFERF_TIMELENGTH, mediaobj/_DMO_INPUT_DATA_BUFFER_FLAGS
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
 - _DMO_INPUT_DATA_BUFFER_FLAGS
 - mediaobj/_DMO_INPUT_DATA_BUFFER_FLAGS
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
 - _DMO_INPUT_DATA_BUFFER_FLAGS
---

# _DMO_INPUT_DATA_BUFFER_FLAGS enumeration


## -description

The <code>DMO_INPUT_DATA_BUFFER_FLAGS</code> enumeration defines flags that describe an input buffer.

## -enum-fields

### -field DMO_INPUT_DATA_BUFFERF_SYNCPOINT:0x1

The beginning of the data is a synchronization point.

### -field DMO_INPUT_DATA_BUFFERF_TIME:0x2

The buffer's time stamp is valid.

The buffer's indicated time length is valid.

### -field DMO_INPUT_DATA_BUFFERF_TIMELENGTH:0x4

The buffer's indicated time length is valid.

### -field DMO_INPUT_DATA_BUFFERF_DISCONTINUITY:0x8

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a>
