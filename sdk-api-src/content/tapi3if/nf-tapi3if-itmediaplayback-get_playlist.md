---
UID: NF:tapi3if.ITMediaPlayback.get_PlayList
title: ITMediaPlayback::get_PlayList
author: windows-sdk-content
description: The get_PlayList method gets the list of files to play.
old-location: tapi3\itmediaplayback_get_playlist.htm
tech.root: tapi
ms.assetid: 57bc8373-0015-4652-bad7-21497d1fd6ff
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITMediaPlayback interface [TAPI 2.2],get_PlayList method, ITMediaPlayback.get_PlayList, ITMediaPlayback::get_PlayList, _tapi3_itmediaplayback_get_playlist, get_PlayList, get_PlayList method [TAPI 2.2], get_PlayList method [TAPI 2.2],ITMediaPlayback interface, tapi3.itmediaplayback_get_playlist, tapi3if/ITMediaPlayback::get_PlayList
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
 - ITMediaPlayback.get_PlayList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66b43721-f902-4a0e-8cbb-418438617f47">ITMediaPlayback</a>



<a href="https://msdn.microsoft.com/685712ef-100f-4f8d-9b1f-c43170c0f197">put_PlayList</a>
 

 

