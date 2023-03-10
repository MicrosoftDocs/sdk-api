---
UID: NF:tapi3if.ITMediaPlayback.put_PlayList
title: ITMediaPlayback::put_PlayList (tapi3if.h)
description: The put_PlayList method provides the file playback terminal with the list of files to play.
helpviewer_keywords: ["ITMediaPlayback interface [TAPI 2.2]","put_PlayList method","ITMediaPlayback.put_PlayList","ITMediaPlayback::put_PlayList","_tapi3_itmediaplayback_put_playlist","put_PlayList","put_PlayList method [TAPI 2.2]","put_PlayList method [TAPI 2.2]","ITMediaPlayback interface","tapi3.itmediaplayback_put_playlist","tapi3if/ITMediaPlayback::put_PlayList"]
old-location: tapi3\itmediaplayback_put_playlist.htm
tech.root: tapi3
ms.assetid: 685712ef-100f-4f8d-9b1f-c43170c0f197
ms.date: 12/05/2018
ms.keywords: ITMediaPlayback interface [TAPI 2.2],put_PlayList method, ITMediaPlayback.put_PlayList, ITMediaPlayback::put_PlayList, _tapi3_itmediaplayback_put_playlist, put_PlayList, put_PlayList method [TAPI 2.2], put_PlayList method [TAPI 2.2],ITMediaPlayback interface, tapi3.itmediaplayback_put_playlist, tapi3if/ITMediaPlayback::put_PlayList
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
 - ITMediaPlayback::put_PlayList
 - tapi3if/ITMediaPlayback::put_PlayList
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
 - ITMediaPlayback.put_PlayList
---

# ITMediaPlayback::put_PlayList


## -description

The 
<b>put_PlayList</b> method provides the file playback terminal with the list of files to play.

## -parameters

### -param PlayListVariant [in]

Variant of type VT_ARRAY, which contains variants of type VT_BSTR and VT_STORAGE. 




The VT_BSTR elements of the array contain the names of the files to play. The file name extension is used to determine the type of file. Currently, the supported file name extensions are .avi and .wav.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback">ITMediaPlayback</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itmediaplayback-get_playlist">get_PlayList</a>