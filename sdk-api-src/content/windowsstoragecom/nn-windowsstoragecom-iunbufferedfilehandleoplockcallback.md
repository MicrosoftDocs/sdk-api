---
UID: NN:windowsstoragecom.IUnbufferedFileHandleOplockCallback
title: IUnbufferedFileHandleOplockCallback (windowsstoragecom.h)
description: Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle method is broken.
helpviewer_keywords: ["IUnbufferedFileHandleOplockCallback","IUnbufferedFileHandleOplockCallback interface [Windows Runtime]","IUnbufferedFileHandleOplockCallback interface [Windows Runtime]","described","windowsstoragecom/IUnbufferedFileHandleOplockCallback","winrt.iunbufferedfilehandleoplockcallback"]
old-location: winrt\iunbufferedfilehandleoplockcallback.htm
tech.root: WinRT
ms.assetid: 7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleOplockCallback, IUnbufferedFileHandleOplockCallback interface [Windows Runtime], IUnbufferedFileHandleOplockCallback interface [Windows Runtime],described, windowsstoragecom/IUnbufferedFileHandleOplockCallback, winrt.iunbufferedfilehandleoplockcallback
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
 - IUnbufferedFileHandleOplockCallback
 - windowsstoragecom/IUnbufferedFileHandleOplockCallback
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
 - IUnbufferedFileHandleOplockCallback
---

# IUnbufferedFileHandleOplockCallback interface


## -description

Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the <a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.

## -inheritance

The <b>IUnbufferedFileHandleOplockCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUnbufferedFileHandleOplockCallback</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
