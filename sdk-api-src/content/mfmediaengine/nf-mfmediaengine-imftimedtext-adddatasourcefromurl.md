---
UID: NF:mfmediaengine.IMFTimedText.AddDataSourceFromUrl
title: IMFTimedText::AddDataSourceFromUrl
author: windows-sdk-content
description: Adds a timed-text data source from the specified URL.
old-location: mf\imftimedtext_adddatasourcefromurl.htm
old-project: medfound
ms.assetid: 5E02BE3F-D0A8-492D-BBB2-F5A95B9C406D
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: AddDataSourceFromUrl, AddDataSourceFromUrl method [Media Foundation], AddDataSourceFromUrl method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],AddDataSourceFromUrl method, IMFTimedText.AddDataSourceFromUrl, IMFTimedText::AddDataSourceFromUrl, mf.imftimedtext_adddatasourcefromurl, mfmediaengine/IMFTimedText::AddDataSourceFromUrl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
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
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
req.product: GDI+ 1.1
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

Type: <b><a href="https://msdn.microsoft.com/FB064449-56D5-48D4-849F-717767F352F5">MF_TIMED_TEXT_TRACK_KIND</a></b>

A <a href="https://msdn.microsoft.com/FB064449-56D5-48D4-849F-717767F352F5">MF_TIMED_TEXT_TRACK_KIND</a>-typed value that specifies the kind of timed-text track.


### -param isDefault [in]

Type: <b>BOOL</b>

Specifies whether to add the default data source. Specify <b>TRUE</b> to add the default data source or <b>FALSE</b> otherwise.


### -param trackId [out]

Type: <b>DWORD*</b>

Receives a pointer to the unique identifier for the added track.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

