---
UID: NF:tapi3if.ITFileTrack.get_Format
title: ITFileTrack::get_Format (tapi3if.h)
description: The get_Format method gets the file terminal's format.
helpviewer_keywords: ["ITFileTrack interface [TAPI 2.2]","get_Format method","ITFileTrack.get_Format","ITFileTrack::get_Format","_tapi3_itfiletrack_get_format","get_Format","get_Format method [TAPI 2.2]","get_Format method [TAPI 2.2]","ITFileTrack interface","tapi3.itfiletrack_get_format","tapi3if/ITFileTrack::get_Format"]
old-location: tapi3\itfiletrack_get_format.htm
tech.root: tapi3
ms.assetid: 6d489888-49b3-4fcd-9643-82f0a08fe1c6
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_Format method, ITFileTrack.get_Format, ITFileTrack::get_Format, _tapi3_itfiletrack_get_format, get_Format, get_Format method [TAPI 2.2], get_Format method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_format, tapi3if/ITFileTrack::get_Format
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITFileTrack::get_Format
 - tapi3if/ITFileTrack::get_Format
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITFileTrack.get_Format
---

# ITFileTrack::get_Format


## -description

The 
<b>get_Format</b> method gets the file terminal's format.

## -parameters

### -param ppmt [out]

Pointer to an 
<b>AM_MEDIA_TYPE</b> descriptor of the terminal format. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>