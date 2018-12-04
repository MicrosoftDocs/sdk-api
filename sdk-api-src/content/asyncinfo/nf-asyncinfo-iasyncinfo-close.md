---
UID: NF:asyncinfo.IAsyncInfo.Close
title: IAsyncInfo::Close
author: windows-sdk-content
description: Closes the asynchronous work object.
old-location: winrt\iasyncinfo_close.htm
tech.root: WinRT
ms.assetid: 1c357343-79cf-4808-8e41-f898dfdb99f6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Close, Close method [Windows Runtime], Close method [Windows Runtime],IAsyncInfo interface, IAsyncInfo interface [Windows Runtime],Close method, IAsyncInfo.Close, IAsyncInfo::Close, asyncinfo/IAsyncInfo::Close, winrt.iasyncinfo_close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncInfo::Close


## -description


Closes the asynchronous work object. Call this method after the results of the operation have been consumed but before calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3444e02e-8817-4c23-84d9-1a2d1bf43a52">IAsyncInfo</a>
 

 

