---
UID: NF:mfidl.IMFNetResourceFilter.OnSendingRequest
title: IMFNetResourceFilter::OnSendingRequest (mfidl.h)
author: windows-sdk-content
description: Called when the byte stream requests a URL.
old-location: mf\imfnetresourcefilter_onsendingrequest.htm
tech.root: medfound
ms.assetid: 4FE6BBE8-A8EC-4304-BC4B-4D49F8EADC25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter interface [Media Foundation],OnSendingRequest method, IMFNetResourceFilter.OnSendingRequest, IMFNetResourceFilter::OnSendingRequest, OnSendingRequest, OnSendingRequest method [Media Foundation], OnSendingRequest method [Media Foundation],IMFNetResourceFilter interface, mf.imfnetresourcefilter_onsendingrequest, mfidl/IMFNetResourceFilter::OnSendingRequest
ms.topic: method
f1_keywords: 
 - "mfidl/IMFNetResourceFilter.OnSendingRequest"
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - mfidl.h
api_name:
 - IMFNetResourceFilter.OnSendingRequest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetResourceFilter::OnSendingRequest


## -description


Called when the byte stream requests a URL.


## -parameters




### -param pszUrl [in]

The URL that the byte stream is requesting.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter">IMFNetResourceFilter</a>
 

 

