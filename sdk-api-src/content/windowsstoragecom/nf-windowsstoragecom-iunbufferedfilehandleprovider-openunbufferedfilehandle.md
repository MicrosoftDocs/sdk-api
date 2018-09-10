---
UID: NF:windowsstoragecom.IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle
title: IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle
author: windows-sdk-content
description: Gets a handle from a random-access byte stream that the StorageFile.OpenAsync method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken.
old-location: winrt\iunbufferedfilehandleprovider_openunbufferedfilehandle.htm
tech.root: WinRT
ms.assetid: D001CD90-A621-403C-B9BD-BE79471AF18F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUnbufferedFileHandleProvider interface [Windows Runtime],OpenUnbufferedFileHandle method, IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle, IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle, OpenUnbufferedFileHandle, OpenUnbufferedFileHandle method [Windows Runtime], OpenUnbufferedFileHandle method [Windows Runtime],IUnbufferedFileHandleProvider interface, windowsstoragecom/IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle, winrt.iunbufferedfilehandleprovider_openunbufferedfilehandle
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
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IUnbufferedFileHandleProvider.OpenUnbufferedFileHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle


## -description


Gets a handle from a random-access byte stream that the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken. 


## -parameters




### -param oplockBreakCallback [in]

An interface that contains the implementation of the <a href="https://msdn.microsoft.com/F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60">IUnbufferedFileHandleOplockCallback::OnBrokenCallback</a> method that you want to run when the opportunistic lock for the handle is broken. 


### -param fileHandle [out, retval]

The handle from the random-access byte stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</b> opens a new handle that is open for GENERIC_READ. <b>IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</b> does not return the actual handle underlying the stream, or a duplicate of that handle.

 Call <a href="https://msdn.microsoft.com/8D6CD3A2-0CCD-49F4-86B3-99823A6E4EA8">IUnbufferedFileHandleProvider::CloseUnbufferedFileHandle</a> when you no longer need the handle. The handle is also closed when the opportunistic lock breaks, so your code must process exceptions that occur when the handle is not valid. 




## -see-also




<a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a>



<a href="https://msdn.microsoft.com/7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3">IUnbufferedFileHandleOplockCallback</a>



<a href="https://msdn.microsoft.com/F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60">IUnbufferedFileHandleOplockCallback::OnBrokenCallback</a>



<a href="https://msdn.microsoft.com/9716B7ED-8E2C-4B7F-B9C9-39A755615CB3">IUnbufferedFileHandleProvider</a>



<a href="https://msdn.microsoft.com/8D6CD3A2-0CCD-49F4-86B3-99823A6E4EA8">IUnbufferedFileHandleProvider::CloseUnbufferedFileHandle</a>
 

 

