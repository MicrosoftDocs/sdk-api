---
UID: NF:windowsstoragecom.IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle
title: IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle (windowsstoragecom.h)
description: Gets a handle from a random-access byte stream that the StorageFile.OpenAsync method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken.
helpviewer_keywords: ["IUnbufferedFileHandleProvider interface [Windows Runtime]","OpenUnbufferedFileHandle method","IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle","IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle","OpenUnbufferedFileHandle","OpenUnbufferedFileHandle method [Windows Runtime]","OpenUnbufferedFileHandle method [Windows Runtime]","IUnbufferedFileHandleProvider interface","windowsstoragecom/IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle","winrt.iunbufferedfilehandleprovider_openunbufferedfilehandle"]
old-location: winrt\iunbufferedfilehandleprovider_openunbufferedfilehandle.htm
tech.root: WinRT
ms.assetid: D001CD90-A621-403C-B9BD-BE79471AF18F
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleProvider interface [Windows Runtime],OpenUnbufferedFileHandle method, IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle, IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle, OpenUnbufferedFileHandle, OpenUnbufferedFileHandle method [Windows Runtime], OpenUnbufferedFileHandle method [Windows Runtime],IUnbufferedFileHandleProvider interface, windowsstoragecom/IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle, winrt.iunbufferedfilehandleprovider_openunbufferedfilehandle
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
 - IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle
 - windowsstoragecom/IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle
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
 - IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle
---

# IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle


## -description

Gets a handle from a random-access byte stream that the <a href="/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a> method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken.

## -parameters

### -param oplockBreakCallback [in]

An interface that contains the implementation of the <a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleoplockcallback-onbrokencallback">IUnbufferedFileHandleOplockCallback::OnBrokenCallback</a> method that you want to run when the opportunistic lock for the handle is broken.

### -param fileHandle [out, retval]

The handle from the random-access byte stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</b> opens a new handle that is open for GENERIC_READ. <b>IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</b> does not return the actual handle underlying the stream, or a duplicate of that handle.

 Call <a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-closeunbufferedfilehandle">IUnbufferedFileHandleProvider::CloseUnbufferedFileHandle</a> when you no longer need the handle. The handle is also closed when the opportunistic lock breaks, so your code must process exceptions that occur when the handle is not valid.

## -see-also

<a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a>



<a href="/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback">IUnbufferedFileHandleOplockCallback</a>



<a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleoplockcallback-onbrokencallback">IUnbufferedFileHandleOplockCallback::OnBrokenCallback</a>



<a href="/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider">IUnbufferedFileHandleProvider</a>



<a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-closeunbufferedfilehandle">IUnbufferedFileHandleProvider::CloseUnbufferedFileHandle</a>