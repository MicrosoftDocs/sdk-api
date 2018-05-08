---
UID: NF:mfidl.IMFNetResourceFilter.OnSendingRequest
title: IMFNetResourceFilter::OnSendingRequest
author: windows-driver-content
description: Called when the byte stream requests a URL.
old-location: mf\imfnetresourcefilter_onsendingrequest.htm
old-project: medfound
ms.assetid: 4FE6BBE8-A8EC-4304-BC4B-4D49F8EADC25
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFNetResourceFilter interface [Media Foundation],OnSendingRequest method, IMFNetResourceFilter.OnSendingRequest, IMFNetResourceFilter::OnSendingRequest, OnSendingRequest, OnSendingRequest method [Media Foundation], OnSendingRequest method [Media Foundation],IMFNetResourceFilter interface, mf.imfnetresourcefilter_onsendingrequest, mfidl/IMFNetResourceFilter::OnSendingRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFNetResourceFilter.OnSendingRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/AC8FBD93-B39B-4530-8475-275D3D0DA512">IMFNetResourceFilter</a>
 

 

