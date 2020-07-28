---
UID: NN:windowsstoragecom.IUnbufferedFileHandleProvider
title: IUnbufferedFileHandleProvider (windowsstoragecom.h)
description: Provides access to handles from a random-access byte stream that the StorageFile.OpenAsync method created.
helpviewer_keywords: ["IUnbufferedFileHandleProvider","IUnbufferedFileHandleProvider interface [Windows Runtime]","IUnbufferedFileHandleProvider interface [Windows Runtime]","described","windowsstoragecom/IUnbufferedFileHandleProvider","winrt.iunbufferedfilehandleprovider"]
old-location: winrt\iunbufferedfilehandleprovider.htm
tech.root: WinRT
ms.assetid: 9716B7ED-8E2C-4B7F-B9C9-39A755615CB3
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleProvider, IUnbufferedFileHandleProvider interface [Windows Runtime], IUnbufferedFileHandleProvider interface [Windows Runtime],described, windowsstoragecom/IUnbufferedFileHandleProvider, winrt.iunbufferedfilehandleprovider
f1_keywords:
- windowsstoragecom/IUnbufferedFileHandleProvider
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
- IUnbufferedFileHandleProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUnbufferedFileHandleProvider interface


## -description


Provides access to handles from a random-access byte stream that the <a href="https://docs.microsoft.com/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a> method created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnbufferedFileHandleProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUnbufferedFileHandleProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUnbufferedFileHandleProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-closeunbufferedfilehandle">CloseUnbufferedFileHandle</a>
</td>
<td align="left" width="63%">
Closes the handle from a random-access byte stream that you created by calling <a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle">OpenUnbufferedFileHandle</a>
</td>
<td align="left" width="63%">
Gets a handle from a random-access byte stream that the <a href="https://docs.microsoft.com/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a> method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a>



<a href="https://docs.microsoft.com/uwp/api/windows.storage.storagefile.openasync">StorageFile.OpenAsync</a>
 

 

