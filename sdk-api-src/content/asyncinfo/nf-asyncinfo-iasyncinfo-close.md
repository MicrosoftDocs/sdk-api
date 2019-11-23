---
UID: NF:asyncinfo.IAsyncInfo.Close
title: IAsyncInfo::Close (asyncinfo.h)

description: Closes the asynchronous work object.
old-location: winrt\iasyncinfo_close.htm
tech.root: WinRT
ms.assetid: 1c357343-79cf-4808-8e41-f898dfdb99f6

ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Runtime], Close method [Windows Runtime],IAsyncInfo interface, IAsyncInfo interface [Windows Runtime],Close method, IAsyncInfo.Close, IAsyncInfo::Close, asyncinfo/IAsyncInfo::Close, winrt.iasyncinfo_close
ms.topic: method
f1_keywords: 
 - "asyncinfo/IAsyncInfo.Close"
dev_langs:
 - c++
req.header: asyncinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AsyncInfo.idl
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
 - AsyncInfo.h
api_name:
 - IAsyncInfo.Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsyncInfo::Close


## -description


Closes the asynchronous work object. Call this method after the results of the operation have been consumed but before calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nn-asyncinfo-iasyncinfo">IAsyncInfo</a>
 

 

