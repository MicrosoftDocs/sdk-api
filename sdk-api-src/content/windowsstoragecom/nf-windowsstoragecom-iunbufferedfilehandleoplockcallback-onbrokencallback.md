---
UID: NF:windowsstoragecom.IUnbufferedFileHandleOplockCallback.OnBrokenCallback
title: IUnbufferedFileHandleOplockCallback::OnBrokenCallback
author: windows-driver-content
description: Runs when the opportunistic lock for a handle that you get by calling the IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle method is broken.
old-location: winrt\iunbufferedfilehandleoplockcallback_onbrokencallback.htm
old-project: WinRT
ms.assetid: F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: IUnbufferedFileHandleOplockCallback interface [Windows Runtime],OnBrokenCallback method, IUnbufferedFileHandleOplockCallback.OnBrokenCallback, IUnbufferedFileHandleOplockCallback::OnBrokenCallback, OnBrokenCallback, OnBrokenCallback method [Windows Runtime], OnBrokenCallback method [Windows Runtime],IUnbufferedFileHandleOplockCallback interface, windowsstoragecom/IUnbufferedFileHandleOplockCallback::OnBrokenCallback, winrt.iunbufferedfilehandleoplockcallback_onbrokencallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.storage.dll
api_name:
-	IUnbufferedFileHandleOplockCallback.OnBrokenCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IUnbufferedFileHandleOplockCallback::OnBrokenCallback


## -description


Runs when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this method to specify what your app should do when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.




## -see-also




<a href="https://msdn.microsoft.com/7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3">IUnbufferedFileHandleOplockCallback</a>



<a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
 

 

