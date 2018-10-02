---
UID: NF:tapi3if.ITMediaPlayback.put_PlayList
title: ITMediaPlayback::put_PlayList
author: windows-sdk-content
description: The put_PlayList method provides the file playback terminal with the list of files to play.
old-location: tapi3\itmediaplayback_put_playlist.htm
tech.root: TAPI
ms.assetid: 685712ef-100f-4f8d-9b1f-c43170c0f197
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITMediaPlayback interface [TAPI 2.2],put_PlayList method, ITMediaPlayback.put_PlayList, ITMediaPlayback::put_PlayList, _tapi3_itmediaplayback_put_playlist, put_PlayList, put_PlayList method [TAPI 2.2], put_PlayList method [TAPI 2.2],ITMediaPlayback interface, tapi3.itmediaplayback_put_playlist, tapi3if/ITMediaPlayback::put_PlayList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/66b43721-f902-4a0e-8cbb-418438617f47">ITMediaPlayback</a>



<a href="https://msdn.microsoft.com/57bc8373-0015-4652-bad7-21497d1fd6ff">get_PlayList</a>
 

 

