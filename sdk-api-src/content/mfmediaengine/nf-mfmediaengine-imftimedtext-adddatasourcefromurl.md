---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C76D087C-7039-4C1F-93D0-0CBAC925EE43">IMFTimedText</a>
 

 

