---
UID: NF:mfmediaengine.IMFTimedText.AddDataSource
title: IMFTimedText::AddDataSource
author: windows-sdk-content
description: Adds a timed-text data source.
old-location: mf\imftimedtext_adddatasource.htm
tech.root: medfound
ms.assetid: 76922DFA-E109-475D-BE09-47501AC7F50E
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddDataSource, AddDataSource method [Media Foundation], AddDataSource method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],AddDataSource method, IMFTimedText.AddDataSource, IMFTimedText::AddDataSource, mf.imftimedtext_adddatasource, mfmediaengine/IMFTimedText::AddDataSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFTimedText.AddDataSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedText::AddDataSource


## -description


Adds a timed-text data source.


## -parameters




### -param byteStream

TBD


### -param label

TBD


### -param language

TBD


### -param kind [in]

Type: <b><a href="https://msdn.microsoft.com/FB064449-56D5-48D4-849F-717767F352F5">MF_TIMED_TEXT_TRACK_KIND</a></b>

A <a href="https://msdn.microsoft.com/FB064449-56D5-48D4-849F-717767F352F5">MF_TIMED_TEXT_TRACK_KIND</a>-typed value that specifies the kind of timed-text track.


### -param isDefault

TBD


### -param trackId [out]

Type: <b>DWORD*</b>

Receives a pointer to the unique identifier for the added track.


#### - fDefault [in]

Type: <b>BOOL</b>

Specifies whether to add the default data source. Specify <b>TRUE</b> to add the default data source or <b>FALSE</b> otherwise.


#### - pByteStream [in]

Type: <b><a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface for the data source to add.


#### - pLabel [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the label of the data source.


#### - pLanguage [in, optional]

Type: <b>LPCWSTR</b>

Null-terminated wide-character string that contains the language of the data source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

