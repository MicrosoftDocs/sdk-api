---
UID: NF:mfidl.IMFNetResourceFilter.OnRedirect
title: IMFNetResourceFilter::OnRedirect (mfidl.h)
author: windows-sdk-content
description: Called when the byte stream redirects to a URL.
old-location: mf\imfnetresourcefilter_onredirect.htm
tech.root: medfound
ms.assetid: 418EA3E0-9732-43B7-BF80-A85ECB7A9485
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter interface [Media Foundation],OnRedirect method, IMFNetResourceFilter.OnRedirect, IMFNetResourceFilter::OnRedirect, OnRedirect, OnRedirect method [Media Foundation], OnRedirect method [Media Foundation],IMFNetResourceFilter interface, mf.imfnetresourcefilter_onredirect, mfidl/IMFNetResourceFilter::OnRedirect
ms.topic: method
f1_keywords: ["mfidl/IMFNetResourceFilter.OnRedirect"]
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
 - IMFNetResourceFilter.OnRedirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetResourceFilter::OnRedirect


## -description


Called when the byte stream redirects to a URL.


## -parameters




### -param pszUrl [in]

The URL to which the connection has been redirected.


### -param pvbCancel [out]

To cancel the redirection, set this parameter to <b>VARIANT_TRUE</b>. To allow the redirection, set this parameter to <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter">IMFNetResourceFilter</a>
 

 

