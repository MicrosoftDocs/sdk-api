---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetDataFormat
title: IMFTimedTextTrack::GetDataFormat (mfmediaengine.h)
description: Gets a GUID that identifies the track's underlying data format.helpviewer_keywords: ["GetDataFormat","GetDataFormat method [Media Foundation]","GetDataFormat method [Media Foundation]","IMFTimedTextTrack interface","IMFTimedTextTrack interface [Media Foundation]","GetDataFormat method","IMFTimedTextTrack.GetDataFormat","IMFTimedTextTrack::GetDataFormat","mf.imftimedtexttrack_getdataformat","mfmediaengine/IMFTimedTextTrack::GetDataFormat"]
old-location: mf\imftimedtexttrack_getdataformat.htm
tech.root: medfound
ms.assetid: B00FA013-1C96-48FB-8046-D9A24BB78412
ms.date: 12/05/2018
ms.keywords: GetDataFormat, GetDataFormat method [Media Foundation], GetDataFormat method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetDataFormat method, IMFTimedTextTrack.GetDataFormat, IMFTimedTextTrack::GetDataFormat, mf.imftimedtexttrack_getdataformat, mfmediaengine/IMFTimedTextTrack::GetDataFormat
f1_keywords:
- mfmediaengine/IMFTimedTextTrack.GetDataFormat
dev_langs:
- c++
req.header: mfmediaengine.h
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
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.dll
api_name:
- IMFTimedTextTrack.GetDataFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextTrack::GetDataFormat


## -description


Gets a GUID that identifies the track's underlying data format.


## -parameters




### -param format [out]

Type: <b>GUID*</b>

A GUID that identifies the track's underlying data format.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>
 

 

