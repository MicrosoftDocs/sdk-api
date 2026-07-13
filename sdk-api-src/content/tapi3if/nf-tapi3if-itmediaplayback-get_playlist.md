---
UID: NF:tapi3if.ITMediaPlayback.get_PlayList
title: ITMediaPlayback::get_PlayList (tapi3if.h)
description: The get_PlayList method gets the list of files to play.
helpviewer_keywords: ["ITMediaPlayback interface [TAPI 2.2]","get_PlayList method","ITMediaPlayback.get_PlayList","ITMediaPlayback::get_PlayList","_tapi3_itmediaplayback_get_playlist","get_PlayList","get_PlayList method [TAPI 2.2]","get_PlayList method [TAPI 2.2]","ITMediaPlayback interface","tapi3.itmediaplayback_get_playlist","tapi3if/ITMediaPlayback::get_PlayList"]
old-location: tapi3\itmediaplayback_get_playlist.htm
tech.root: tapi3
ms.assetid: 57bc8373-0015-4652-bad7-21497d1fd6ff
ms.date: 12/05/2018
ms.keywords: ITMediaPlayback interface [TAPI 2.2],get_PlayList method, ITMediaPlayback.get_PlayList, ITMediaPlayback::get_PlayList, _tapi3_itmediaplayback_get_playlist, get_PlayList, get_PlayList method [TAPI 2.2], get_PlayList method [TAPI 2.2],ITMediaPlayback interface, tapi3.itmediaplayback_get_playlist, tapi3if/ITMediaPlayback::get_PlayList
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
 - ITMediaPlayback::get_PlayList
 - tapi3if/ITMediaPlayback::get_PlayList
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
 - ITMediaPlayback.get_PlayList
---

# ITMediaPlayback::get_PlayList


## -description

The 
<b>get_PlayList</b> method gets the list of files to play.

## -parameters

### -param pPlayListVariant [out]

Pointer to variant of type VT_ARRAY, which contains variants of type VT_BSTR and VT_STORAGE. 




The VT_BSTR elements of the array contain the names of the files to play. The file name extension is used to specify the type of file. Currently, supported file name extensions are .avi and .wav.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback">ITMediaPlayback</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itmediaplayback-put_playlist">put_PlayList</a>