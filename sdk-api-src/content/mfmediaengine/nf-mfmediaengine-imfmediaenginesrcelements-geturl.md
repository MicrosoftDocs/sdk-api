---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.GetURL
title: IMFMediaEngineSrcElements::GetURL
author: windows-sdk-content
description: Gets the URL of an element in the list.
old-location: mf\imfmediaenginesrcelements_geturl.htm
old-project: medfound
ms.assetid: 5935BE0D-0E5A-46A8-944C-096746C5FCA3
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFMediaEngineSrcElements interface, IMFMediaEngineSrcElements interface [Media Foundation],GetURL method, IMFMediaEngineSrcElements.GetURL, IMFMediaEngineSrcElements::GetURL, mf.imfmediaenginesrcelements_geturl, mfmediaengine/IMFMediaEngineSrcElements::GetURL
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSrcElements.GetURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineSrcElements::GetURL


## -description


Gets the URL of an element in the list.


## -parameters




### -param index [in]

The zero-based index of the source element. To get the number of source elements, call <a href="https://msdn.microsoft.com/212883A5-5613-4BCC-8713-9CD5E6480136">IMFMediaEngineSrcElements::GetLength</a>.


### -param pURL [out]

Receives a <b>BSTR</b> that contains the URL of the source element. The caller must free the  <b>BSTR</b> by calling <b>SysFreeString</b>. If no URL is set, this parameter receives the value <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3">IMFMediaEngineSrcElements</a>
 

 

