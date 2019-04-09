---
UID: NN:windowsstoragecom.IUnbufferedFileHandleProvider
title: IUnbufferedFileHandleProvider (windowsstoragecom.h)
author: windows-sdk-content
description: Provides access to handles from a random-access byte stream that the StorageFile.OpenAsync method created.
old-location: winrt\iunbufferedfilehandleprovider.htm
tech.root: WinRT
ms.assetid: 9716B7ED-8E2C-4B7F-B9C9-39A755615CB3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUnbufferedFileHandleProvider, IUnbufferedFileHandleProvider interface [Windows Runtime], IUnbufferedFileHandleProvider interface [Windows Runtime],described, windowsstoragecom/IUnbufferedFileHandleProvider, winrt.iunbufferedfilehandleprovider
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnbufferedFileHandleProvider interface


## -description


Provides access to handles from a random-access byte stream that the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnbufferedFileHandleProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUnbufferedFileHandleProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8D6CD3A2-0CCD-49F4-86B3-99823A6E4EA8">CloseUnbufferedFileHandle</a>
</td>
<td align="left" width="63%">
Closes the handle from a random-access byte stream that you created by calling <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">OpenUnbufferedFileHandle</a>
</td>
<td align="left" width="63%">
Gets a handle from a random-access byte stream that the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method created and registers a callback method that you want to run when the opportunistic lock for the handle is broken. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a>



<a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a>
 

 

