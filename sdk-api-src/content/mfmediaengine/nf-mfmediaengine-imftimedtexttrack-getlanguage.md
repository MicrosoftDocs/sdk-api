---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetLanguage
title: IMFTimedTextTrack::GetLanguage (mfmediaengine.h)
description: Gets the language of the track.
old-location: mf\imftimedtexttrack_getlanguage.htm
tech.root: medfound
ms.assetid: 5676082D-A3D2-4239-A73F-65FA77D660EF
ms.date: 12/05/2018
ms.keywords: GetLanguage, GetLanguage method [Media Foundation], GetLanguage method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetLanguage method, IMFTimedTextTrack.GetLanguage, IMFTimedTextTrack::GetLanguage, mf.imftimedtexttrack_getlanguage, mfmediaengine/IMFTimedTextTrack::GetLanguage
ms.topic: method
f1_keywords:
- mfmediaengine/IMFTimedTextTrack.GetLanguage
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFTimedTextTrack.GetLanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextTrack::GetLanguage


## -description


Gets the language of the track.


## -parameters




### -param language [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the language of the track.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>
 

 

