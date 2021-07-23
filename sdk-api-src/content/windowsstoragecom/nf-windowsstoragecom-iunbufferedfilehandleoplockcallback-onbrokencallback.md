---
UID: NF:windowsstoragecom.IUnbufferedFileHandleOplockCallback.OnBrokenCallback
title: IUnbufferedFileHandleOplockCallback::OnBrokenCallback (windowsstoragecom.h)
description: Runs when the opportunistic lock for a handle that you get by calling the IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle method is broken.
helpviewer_keywords: ["IUnbufferedFileHandleOplockCallback interface [Windows Runtime]","OnBrokenCallback method","IUnbufferedFileHandleOplockCallback.OnBrokenCallback","IUnbufferedFileHandleOplockCallback::OnBrokenCallback","OnBrokenCallback","OnBrokenCallback method [Windows Runtime]","OnBrokenCallback method [Windows Runtime]","IUnbufferedFileHandleOplockCallback interface","windowsstoragecom/IUnbufferedFileHandleOplockCallback::OnBrokenCallback","winrt.iunbufferedfilehandleoplockcallback_onbrokencallback"]
old-location: winrt\iunbufferedfilehandleoplockcallback_onbrokencallback.htm
tech.root: WinRT
ms.assetid: F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleOplockCallback interface [Windows Runtime],OnBrokenCallback method, IUnbufferedFileHandleOplockCallback.OnBrokenCallback, IUnbufferedFileHandleOplockCallback::OnBrokenCallback, OnBrokenCallback, OnBrokenCallback method [Windows Runtime], OnBrokenCallback method [Windows Runtime],IUnbufferedFileHandleOplockCallback interface, windowsstoragecom/IUnbufferedFileHandleOplockCallback::OnBrokenCallback, winrt.iunbufferedfilehandleoplockcallback_onbrokencallback
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Windows.storage.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnbufferedFileHandleOplockCallback::OnBrokenCallback
 - windowsstoragecom/IUnbufferedFileHandleOplockCallback::OnBrokenCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IUnbufferedFileHandleOplockCallback.OnBrokenCallback
---

# IUnbufferedFileHandleOplockCallback::OnBrokenCallback


## -description

Runs when the opportunistic lock for a handle that you get by calling the <a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implement this method to specify what your app should do when the opportunistic lock for a handle that you get by calling the <a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.

## -see-also

<a href="/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback">IUnbufferedFileHandleOplockCallback</a>



<a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
