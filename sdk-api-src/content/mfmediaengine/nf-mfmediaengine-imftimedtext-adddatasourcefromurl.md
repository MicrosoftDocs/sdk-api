---
UID: NF:mfmediaengine.IMFTimedText.AddDataSourceFromUrl
title: IMFTimedText::AddDataSourceFromUrl (mfmediaengine.h)
author: windows-sdk-content
description: Adds a timed-text data source from the specified URL.
old-location: mf\imftimedtext_adddatasourcefromurl.htm
tech.root: medfound
ms.assetid: 5E02BE3F-D0A8-492D-BBB2-F5A95B9C406D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddDataSourceFromUrl, AddDataSourceFromUrl method [Media Foundation], AddDataSourceFromUrl method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],AddDataSourceFromUrl method, IMFTimedText.AddDataSourceFromUrl, IMFTimedText::AddDataSourceFromUrl, mf.imftimedtext_adddatasourcefromurl, mfmediaengine/IMFTimedText::AddDataSourceFromUrl
ms.topic: method
f1_keywords: ["mfmediaengine/IMFTimedText.AddDataSourceFromUrl"]
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
 - IMFTimedText.AddDataSourceFromUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedText::AddDataSourceFromUrl


## -description


Adds a timed-text data source from the specified URL.


## -parameters




### -param url [in]

Type: <b>LPCWSTR</b>

The URL of the timed-text data source.


### -param label [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the label of the data source.


### -param language [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the language of the data source.


### -param kind [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_track_kind">MF_TIMED_TEXT_TRACK_KIND</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_track_kind">MF_TIMED_TEXT_TRACK_KIND</a>-typed value that specifies the kind of timed-text track.


### -param isDefault [in]

Type: <b>BOOL</b>

Specifies whether to add the default data source. Specify <b>TRUE</b> to add the default data source or <b>FALSE</b> otherwise.


### -param trackId [out]

Type: <b>DWORD*</b>

Receives a pointer to the unique identifier for the added track.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>
 

 

