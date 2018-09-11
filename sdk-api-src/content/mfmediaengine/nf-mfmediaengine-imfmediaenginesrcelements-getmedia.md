---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.GetMedia
title: IMFMediaEngineSrcElements::GetMedia
author: windows-sdk-content
description: Gets the intended media type of an element in the list.
old-location: mf\imfmediaenginesrcelements_getmedia.htm
tech.root: medfound
ms.assetid: AC99D8D0-ACA6-4FE9-A061-1D3A7D92E596
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetMedia, GetMedia method [Media Foundation], GetMedia method [Media Foundation],IMFMediaEngineSrcElements interface, IMFMediaEngineSrcElements interface [Media Foundation],GetMedia method, IMFMediaEngineSrcElements.GetMedia, IMFMediaEngineSrcElements::GetMedia, mf.imfmediaenginesrcelements_getmedia, mfmediaengine/IMFMediaEngineSrcElements::GetMedia
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFMediaEngineSrcElements.GetMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineSrcElements::GetMedia


## -description


Gets the intended media type of an element in the list.


## -parameters




### -param index [in]

The zero-based index of the source element. To get the number of source elements, call <a href="https://msdn.microsoft.com/212883A5-5613-4BCC-8713-9CD5E6480136">IMFMediaEngineSrcElements::GetLength</a>.


### -param pMedia [out]

Receives a <b>BSTR</b> that contains a media-query string. The caller must free the  <b>BSTR</b> by calling <b>SysFreeString</b>. If no media type is set, this parameter receives the value <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string returned in <i>pMedia</i> should be a media-query string that conforms to the W3C <i>Media Queries</i> specification.




## -see-also




<a href="https://msdn.microsoft.com/37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3">IMFMediaEngineSrcElements</a>
 

 

