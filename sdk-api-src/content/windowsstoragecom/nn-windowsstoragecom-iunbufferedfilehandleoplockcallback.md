---
UID: NN:windowsstoragecom.IUnbufferedFileHandleOplockCallback
title: IUnbufferedFileHandleOplockCallback (windowsstoragecom.h)
description: Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle method is broken.
old-location: winrt\iunbufferedfilehandleoplockcallback.htm
tech.root: WinRT
ms.assetid: 7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleOplockCallback, IUnbufferedFileHandleOplockCallback interface [Windows Runtime], IUnbufferedFileHandleOplockCallback interface [Windows Runtime],described, windowsstoragecom/IUnbufferedFileHandleOplockCallback, winrt.iunbufferedfilehandleoplockcallback
ms.topic: interface
f1_keywords:
- windowsstoragecom/IUnbufferedFileHandleOplockCallback
dev_langs:
- c++
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
- IUnbufferedFileHandleOplockCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUnbufferedFileHandleOplockCallback interface


## -description


Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the <a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnbufferedFileHandleOplockCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUnbufferedFileHandleOplockCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUnbufferedFileHandleOplockCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleoplockcallback-onbrokencallback">OnBrokenCallback</a>
</td>
<td align="left" width="63%">
Runs when the opportunistic lock for a handle that you get by calling the <a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
 

 

