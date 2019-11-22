---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.GetURL
title: IMFMediaEngineSrcElements::GetURL (mfmediaengine.h)

description: Gets the URL of an element in the list.
old-location: mf\imfmediaenginesrcelements_geturl.htm
tech.root: medfound
ms.assetid: 5935BE0D-0E5A-46A8-944C-096746C5FCA3

ms.date: 12/05/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFMediaEngineSrcElements interface, IMFMediaEngineSrcElements interface [Media Foundation],GetURL method, IMFMediaEngineSrcElements.GetURL, IMFMediaEngineSrcElements::GetURL, mf.imfmediaenginesrcelements_geturl, mfmediaengine/IMFMediaEngineSrcElements::GetURL
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineSrcElements.GetURL"
dev_langs:
 - c++
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
 - IMFMediaEngineSrcElements.GetURL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineSrcElements::GetURL


## -description


Gets the URL of an element in the list.


## -parameters




### -param index [in]

The zero-based index of the source element. To get the number of source elements, call <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-getlength">IMFMediaEngineSrcElements::GetLength</a>.


### -param pURL [out]

Receives a <b>BSTR</b> that contains the URL of the source element. The caller must free the  <b>BSTR</b> by calling <b>SysFreeString</b>. If no URL is set, this parameter receives the value <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a>
 

 

