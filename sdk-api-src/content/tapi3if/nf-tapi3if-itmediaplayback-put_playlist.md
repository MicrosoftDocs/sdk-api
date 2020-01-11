---
UID: NF:tapi3if.ITMediaPlayback.put_PlayList
title: ITMediaPlayback::put_PlayList (tapi3if.h)
description: The put_PlayList method provides the file playback terminal with the list of files to play.
old-location: tapi3\itmediaplayback_put_playlist.htm
tech.root: Tapi
ms.assetid: 685712ef-100f-4f8d-9b1f-c43170c0f197
ms.date: 12/05/2018
ms.keywords: ITMediaPlayback interface [TAPI 2.2],put_PlayList method, ITMediaPlayback.put_PlayList, ITMediaPlayback::put_PlayList, _tapi3_itmediaplayback_put_playlist, put_PlayList, put_PlayList method [TAPI 2.2], put_PlayList method [TAPI 2.2],ITMediaPlayback interface, tapi3.itmediaplayback_put_playlist, tapi3if/ITMediaPlayback::put_PlayList
f1_keywords:
- tapi3if/ITMediaPlayback.put_PlayList
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITMediaPlayback.put_PlayList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback">ITMediaPlayback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediaplayback-get_playlist">get_PlayList</a>
 

 

