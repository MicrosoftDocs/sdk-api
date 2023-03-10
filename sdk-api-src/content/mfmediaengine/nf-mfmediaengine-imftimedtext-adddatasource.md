---
UID: NF:mfmediaengine.IMFTimedText.AddDataSource
title: IMFTimedText::AddDataSource (mfmediaengine.h)
description: Adds a timed-text data source.
helpviewer_keywords: ["AddDataSource","AddDataSource method [Media Foundation]","AddDataSource method [Media Foundation]","IMFTimedText interface","IMFTimedText interface [Media Foundation]","AddDataSource method","IMFTimedText.AddDataSource","IMFTimedText::AddDataSource","mf.imftimedtext_adddatasource","mfmediaengine/IMFTimedText::AddDataSource"]
old-location: mf\imftimedtext_adddatasource.htm
tech.root: mf
ms.assetid: 76922DFA-E109-475D-BE09-47501AC7F50E
ms.date: 12/05/2018
ms.keywords: AddDataSource, AddDataSource method [Media Foundation], AddDataSource method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],AddDataSource method, IMFTimedText.AddDataSource, IMFTimedText::AddDataSource, mf.imftimedtext_adddatasource, mfmediaengine/IMFTimedText::AddDataSource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimedText::AddDataSource
 - mfmediaengine/IMFTimedText::AddDataSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedText.AddDataSource
---

# IMFTimedText::AddDataSource


## -description

Adds a timed-text data source.

## -parameters

### -param byteStream [in]

Type: <b><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface for the data source to add.

### -param label [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the label of the data source.

### -param language [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the language of the data source.

### -param kind [in]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_track_kind">MF_TIMED_TEXT_TRACK_KIND</a></b>

A <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_track_kind">MF_TIMED_TEXT_TRACK_KIND</a>-typed value that specifies the kind of timed-text track.

### -param isDefault [in]

Type: <b>BOOL</b>

Specifies whether to add the default data source. Specify <b>TRUE</b> to add the default data source or <b>FALSE</b> otherwise.

### -param trackId [out]

Type: <b>DWORD*</b>

Receives a pointer to the unique identifier for the added track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>